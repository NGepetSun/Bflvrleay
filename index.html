<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>StreamForge — Overlay Generator</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Exo+2:wght@300;400;600;800;900&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #060810;
    --surface: #0d1117;
    --surface2: #161b22;
    --border: rgba(255,255,255,0.06);
    --accent: #00d4ff;
    --accent2: #ff3366;
    --accent3: #7c3aed;
    --text: #e6edf3;
    --muted: #7d8590;
    --glow: rgba(0,212,255,0.15);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Exo 2', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Background grid */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  /* Ambient glow blobs */
  .blob {
    position: fixed;
    border-radius: 50%;
    filter: blur(120px);
    pointer-events: none;
    z-index: 0;
    opacity: 0.12;
  }
  .blob-1 { width:600px; height:600px; background:#00d4ff; top:-200px; right:-100px; }
  .blob-2 { width:400px; height:400px; background:#7c3aed; bottom:-100px; left:-100px; }

  /* Header */
  header {
    position: relative;
    z-index: 10;
    padding: 20px 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid var(--border);
    background: rgba(6,8,16,0.8);
    backdrop-filter: blur(20px);
  }

  .logo {
    font-family: 'Rajdhani', sans-serif;
    font-size: 28px;
    font-weight: 700;
    letter-spacing: 2px;
    background: linear-gradient(135deg, #00d4ff, #7c3aed);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .logo span { color: var(--accent2); -webkit-text-fill-color: var(--accent2); }

  .badge {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    padding: 4px 12px;
    border: 1px solid var(--accent);
    color: var(--accent);
    border-radius: 2px;
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  /* Main layout */
  .app {
    position: relative;
    z-index: 5;
    display: grid;
    grid-template-columns: 360px 1fr;
    height: calc(100vh - 70px);
    overflow: hidden;
  }

  /* Sidebar */
  .sidebar {
    background: rgba(13,17,23,0.95);
    border-right: 1px solid var(--border);
    overflow-y: auto;
    padding: 24px;
    scrollbar-width: thin;
    scrollbar-color: var(--surface2) transparent;
  }

  .sidebar::-webkit-scrollbar { width: 4px; }
  .sidebar::-webkit-scrollbar-track { background: transparent; }
  .sidebar::-webkit-scrollbar-thumb { background: var(--surface2); border-radius: 2px; }

  .section-title {
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 3px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 16px;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border);
  }

  .form-group {
    margin-bottom: 16px;
  }

  label {
    display: block;
    font-size: 12px;
    font-weight: 600;
    color: var(--muted);
    margin-bottom: 6px;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  input[type="text"], select {
    width: 100%;
    background: var(--surface2);
    border: 1px solid var(--border);
    color: var(--text);
    padding: 10px 14px;
    font-family: 'Exo 2', sans-serif;
    font-size: 14px;
    border-radius: 4px;
    outline: none;
    transition: border-color 0.2s;
  }

  input[type="text"]:focus, select:focus {
    border-color: var(--accent);
    box-shadow: 0 0 0 2px rgba(0,212,255,0.1);
  }

  select option { background: #0d1117; }

  /* Theme picker */
  .theme-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
    margin-bottom: 20px;
  }

  .theme-btn {
    aspect-ratio: 16/9;
    border-radius: 6px;
    border: 2px solid transparent;
    cursor: pointer;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
  }

  .theme-btn:hover { transform: scale(1.05); }
  .theme-btn.active { border-color: var(--accent); box-shadow: 0 0 12px var(--glow); }
  .theme-btn .theme-label {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    background: rgba(0,0,0,0.7);
    font-size: 9px;
    text-align: center;
    padding: 3px;
    font-family: 'Share Tech Mono', monospace;
    letter-spacing: 1px;
    color: #fff;
  }

  /* Color swatch */
  .color-row {
    display: flex;
    gap: 8px;
    margin-bottom: 20px;
  }

  .swatch {
    width: 32px; height: 32px;
    border-radius: 50%;
    cursor: pointer;
    border: 2px solid transparent;
    transition: all 0.2s;
    flex-shrink: 0;
  }
  .swatch.active { border-color: white; transform: scale(1.2); }

  /* Buttons */
  .btn-generate {
    width: 100%;
    padding: 14px;
    background: linear-gradient(135deg, #00d4ff, #7c3aed);
    border: none;
    color: white;
    font-family: 'Rajdhani', sans-serif;
    font-size: 16px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
    margin-bottom: 10px;
  }

  .btn-generate::before {
    content: '';
    position: absolute;
    inset: 0;
    background: rgba(255,255,255,0.1);
    transform: translateX(-100%);
    transition: transform 0.3s;
  }
  .btn-generate:hover::before { transform: translateX(100%); }
  .btn-generate:hover { box-shadow: 0 0 30px rgba(0,212,255,0.4); }
  .btn-generate:active { transform: scale(0.98); }

  .btn-download {
    width: 100%;
    padding: 12px;
    background: transparent;
    border: 1px solid var(--accent);
    color: var(--accent);
    font-family: 'Rajdhani', sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s;
  }
  .btn-download:hover { background: rgba(0,212,255,0.1); }

  /* Preview area */
  .preview-area {
    background: #0a0a0f;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }

  .preview-toolbar {
    padding: 12px 20px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 16px;
    background: rgba(13,17,23,0.5);
    flex-shrink: 0;
  }

  .preview-label {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 2px;
    color: var(--muted);
  }

  .dot { width:8px; height:8px; border-radius:50%; }
  .dot-green { background:#2dba4e; }
  .dot-yellow { background:#f1c232; }
  .dot-red { background:#ff3366; }

  .preview-canvas-wrap {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 30px;
    overflow: hidden;
  }

  #overlayCanvas {
    max-width: 100%;
    max-height: 100%;
    border-radius: 4px;
    box-shadow: 0 0 60px rgba(0,0,0,0.8), 0 0 0 1px rgba(255,255,255,0.05);
  }

  .loading-overlay {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(6,8,16,0.85);
    z-index: 20;
  }

  .spinner {
    width: 40px; height: 40px;
    border: 2px solid var(--border);
    border-top-color: var(--accent);
    border-radius: 50%;
    animation: spin 0.8s linear infinite;
  }

  @keyframes spin { to { transform: rotate(360deg); } }

  .section-block {
    margin-bottom: 28px;
  }

  /* Toggle */
  .toggle-group {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    margin-bottom: 16px;
  }

  .toggle-btn {
    padding: 6px 14px;
    border-radius: 3px;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--muted);
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 1px;
    cursor: pointer;
    transition: all 0.2s;
  }

  .toggle-btn.active {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0,212,255,0.08);
  }

  .separator { height: 1px; background: var(--border); margin: 20px 0; }

  /* Variation chips */
  .variation-row {
    display: flex;
    gap: 8px;
    overflow-x: auto;
    padding-bottom: 8px;
    scrollbar-width: none;
  }
  .variation-row::-webkit-scrollbar { display: none; }

  .var-chip {
    flex-shrink: 0;
    padding: 8px 16px;
    border-radius: 3px;
    border: 1px solid var(--border);
    background: var(--surface2);
    cursor: pointer;
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 1px;
    color: var(--muted);
    transition: all 0.2s;
    white-space: nowrap;
  }

  .var-chip:hover { border-color: var(--accent); color: var(--accent); }
  .var-chip.active {
    border-color: var(--accent2);
    color: var(--accent2);
    background: rgba(255,51,102,0.08);
  }

  input[type="color"] {
    -webkit-appearance: none;
    width: 36px; height: 36px;
    border: 1px solid var(--border);
    border-radius: 4px;
    cursor: pointer;
    padding: 2px;
    background: var(--surface2);
  }

  .color-custom-row { display: flex; gap: 8px; align-items: center; margin-bottom: 16px; }
  .color-custom-row label { margin: 0; white-space: nowrap; }
</style>
</head>
<body>

<div class="blob blob-1"></div>
<div class="blob blob-2"></div>

<header>
  <div class="logo">STREAM<span>FORGE</span></div>
  <div style="display:flex;gap:16px;align-items:center">
    <div class="badge">Overlay Generator</div>
  </div>
</header>

<div class="app">
  <!-- SIDEBAR -->
  <div class="sidebar">

    <div class="section-block">
      <div class="section-title">// Channel Info</div>
      <div class="form-group">
        <label>Channel Name</label>
        <input type="text" id="channelName" value="YourChannel" placeholder="Enter channel name">
      </div>
      <div class="form-group">
        <label>Tagline</label>
        <input type="text" id="tagline" value="LIVE GAMING" placeholder="Tagline or category">
      </div>
      <div class="form-group">
        <label>Social Handle</label>
        <input type="text" id="social" value="@yourchannel" placeholder="@handle">
      </div>
    </div>

    <div class="separator"></div>

    <div class="section-block">
      <div class="section-title">// Design Theme</div>
      <div class="theme-grid" id="themeGrid">
        <div class="theme-btn active" data-theme="cyber" style="background: linear-gradient(135deg,#001020,#002040)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(0,212,255,0.3));border-radius:4px"></div>
          <div class="theme-label">CYBER</div>
        </div>
        <div class="theme-btn" data-theme="neon" style="background: linear-gradient(135deg,#1a0020,#300040)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(180,0,255,0.4));border-radius:4px"></div>
          <div class="theme-label">NEON</div>
        </div>
        <div class="theme-btn" data-theme="fire" style="background: linear-gradient(135deg,#1a0800,#301500)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(255,80,0,0.4));border-radius:4px"></div>
          <div class="theme-label">FIRE</div>
        </div>
        <div class="theme-btn" data-theme="forest" style="background: linear-gradient(135deg,#001a08,#002810)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(0,255,100,0.3));border-radius:4px"></div>
          <div class="theme-label">FOREST</div>
        </div>
        <div class="theme-btn" data-theme="gold" style="background: linear-gradient(135deg,#1a1200,#2a1e00)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(255,200,0,0.4));border-radius:4px"></div>
          <div class="theme-label">GOLD</div>
        </div>
        <div class="theme-btn" data-theme="ice" style="background: linear-gradient(135deg,#001520,#002535)">
          <div style="position:absolute;inset:0;background:linear-gradient(45deg,transparent 40%,rgba(150,230,255,0.35));border-radius:4px"></div>
          <div class="theme-label">ICE</div>
        </div>
      </div>
    </div>

    <div class="separator"></div>

    <div class="section-block">
      <div class="section-title">// Layout Style</div>
      <div class="variation-row" id="layoutRow">
        <div class="var-chip active" data-layout="full">FULL PACK</div>
        <div class="var-chip" data-layout="minimal">MINIMAL</div>
        <div class="var-chip" data-layout="panels">PANELS</div>
        <div class="var-chip" data-layout="screens">SCREENS</div>
      </div>
    </div>

    <div class="separator"></div>

    <div class="section-block">
      <div class="section-title">// Accent Color</div>
      <div class="color-row">
        <div class="swatch active" data-color="#00d4ff" style="background:#00d4ff"></div>
        <div class="swatch" data-color="#ff3366" style="background:#ff3366"></div>
        <div class="swatch" data-color="#7c3aed" style="background:#7c3aed"></div>
        <div class="swatch" data-color="#00ff88" style="background:#00ff88"></div>
        <div class="swatch" data-color="#ff6600" style="background:#ff6600"></div>
        <div class="swatch" data-color="#ffd700" style="background:#ffd700"></div>
      </div>
      <div class="color-custom-row">
        <label>Custom:</label>
        <input type="color" id="customColor" value="#00d4ff">
      </div>
    </div>

    <div class="separator"></div>

    <div class="section-block">
      <div class="section-title">// Platform</div>
      <div class="toggle-group" id="platformGroup">
        <button class="toggle-btn active" data-platform="twitch">TWITCH</button>
        <button class="toggle-btn" data-platform="youtube">YOUTUBE</button>
        <button class="toggle-btn" data-platform="kick">KICK</button>
      </div>
    </div>

    <div class="separator"></div>

    <button class="btn-generate" id="generateBtn" onclick="generateOverlay()">
      ⚡ GENERATE OVERLAY
    </button>
    <button class="btn-download" onclick="downloadOverlay()">
      ↓ DOWNLOAD PNG
    </button>

  </div>

  <!-- PREVIEW -->
  <div class="preview-area" style="position:relative">
    <div class="preview-toolbar">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <div class="preview-label">LIVE PREVIEW — 1280×720</div>
    </div>
    <div class="preview-canvas-wrap">
      <canvas id="overlayCanvas" width="1280" height="720"></canvas>
    </div>
  </div>
</div>

<script>
// =============================================
// STATE
// =============================================
let state = {
  channelName: 'YourChannel',
  tagline: 'LIVE GAMING',
  social: '@yourchannel',
  theme: 'cyber',
  layout: 'full',
  accentColor: '#00d4ff',
  platform: 'twitch',
  seed: Math.random()
};

// =============================================
// THEME PALETTES
// =============================================
const themes = {
  cyber:  { bg1: '#060d1a', bg2: '#0a1628', accent: '#00d4ff', accent2: '#0066aa', glow: 'rgba(0,212,255,0.6)', panel: '#0d1e35', text: '#e0f4ff' },
  neon:   { bg1: '#0d0014', bg2: '#180022', accent: '#cc00ff', accent2: '#6600aa', glow: 'rgba(200,0,255,0.6)', panel: '#1a0028', text: '#f0d0ff' },
  fire:   { bg1: '#120500', bg2: '#1e0800', accent: '#ff5500', accent2: '#aa2200', glow: 'rgba(255,100,0,0.6)', panel: '#200a00', text: '#ffe4cc' },
  forest: { bg1: '#011208', bg2: '#031e0c', accent: '#00ff66', accent2: '#008833', glow: 'rgba(0,255,100,0.5)', panel: '#042212', text: '#ccffe0' },
  gold:   { bg1: '#0d0a00', bg2: '#1a1200', accent: '#ffcc00', accent2: '#aa8800', glow: 'rgba(255,200,0,0.5)', panel: '#1e1500', text: '#fff5cc' },
  ice:    { bg1: '#00101e', bg2: '#001828', accent: '#88eeff', accent2: '#4499bb', glow: 'rgba(150,235,255,0.5)', panel: '#001c2e', text: '#e0f8ff' },
};

// =============================================
// CANVAS HELPERS
// =============================================
const canvas = document.getElementById('overlayCanvas');
const ctx = canvas.getContext('2d');

function hexToRgba(hex, alpha) {
  const r = parseInt(hex.slice(1,3),16);
  const g = parseInt(hex.slice(3,5),16);
  const b = parseInt(hex.slice(5,7),16);
  return `rgba(${r},${g},${b},${alpha})`;
}

function lerp(a,b,t){ return a + (b-a)*t; }

// Seeded random
function seededRand(seed) {
  let s = seed;
  return function() {
    s = (s * 9301 + 49297) % 233280;
    return s / 233280;
  };
}

// Draw glowing line
function glowLine(x1,y1,x2,y2, color, width=1, blur=8) {
  ctx.save();
  ctx.shadowColor = color;
  ctx.shadowBlur = blur;
  ctx.strokeStyle = color;
  ctx.lineWidth = width;
  ctx.beginPath();
  ctx.moveTo(x1,y1);
  ctx.lineTo(x2,y2);
  ctx.stroke();
  ctx.restore();
}

// Draw rounded rect
function roundRect(x,y,w,h,r,fill,stroke,strokeW=1) {
  ctx.beginPath();
  ctx.moveTo(x+r,y);
  ctx.lineTo(x+w-r,y);
  ctx.quadraticCurveTo(x+w,y,x+w,y+r);
  ctx.lineTo(x+w,y+h-r);
  ctx.quadraticCurveTo(x+w,y+h,x+w-r,y+h);
  ctx.lineTo(x+r,y+h);
  ctx.quadraticCurveTo(x,y+h,x,y+h-r);
  ctx.lineTo(x,y+r);
  ctx.quadraticCurveTo(x,y,x+r,y);
  ctx.closePath();
  if(fill) { ctx.fillStyle=fill; ctx.fill(); }
  if(stroke) { ctx.strokeStyle=stroke; ctx.lineWidth=strokeW; ctx.stroke(); }
}

function glowRect(x,y,w,h,r,color,alpha=0.4) {
  ctx.save();
  ctx.shadowColor = color;
  ctx.shadowBlur = 20;
  roundRect(x,y,w,h,r,null,color,1.5);
  ctx.restore();
}

// Hexagon pattern bg
function drawHexBg(pal, rand) {
  const size = 18;
  const cols = Math.ceil(1280/size/1.732)+2;
  const rows = Math.ceil(720/size/1.5)+2;
  ctx.save();
  ctx.globalAlpha = 0.08;
  ctx.strokeStyle = pal.accent;
  ctx.lineWidth = 0.5;
  for(let row=0; row<rows; row++) {
    for(let col=0; col<cols; col++) {
      const x = col * size*1.732 + (row%2)*size*0.866;
      const y = row * size*1.5;
      ctx.beginPath();
      for(let i=0;i<6;i++) {
        const angle = Math.PI/3*i - Math.PI/6;
        const px = x + size*Math.cos(angle);
        const py = y + size*Math.sin(angle);
        i===0 ? ctx.moveTo(px,py) : ctx.lineTo(px,py);
      }
      ctx.closePath();
      ctx.stroke();
    }
  }
  ctx.restore();
}

// Circuit lines
function drawCircuitLines(pal, rand) {
  ctx.save();
  ctx.globalAlpha = 0.15;
  for(let i=0;i<14;i++) {
    const x = rand()*1280;
    const y = rand()*720;
    const len = 40 + rand()*120;
    const dir = rand() > 0.5 ? 1 : 0;
    ctx.strokeStyle = pal.accent;
    ctx.lineWidth = 0.8;
    ctx.shadowColor = pal.accent;
    ctx.shadowBlur = 4;
    ctx.beginPath();
    ctx.moveTo(x,y);
    if(dir === 0) {
      ctx.lineTo(x+len, y);
      ctx.lineTo(x+len, y + 20*(rand()>0.5?1:-1));
    } else {
      ctx.lineTo(x, y+len);
      ctx.lineTo(x + 20*(rand()>0.5?1:-1), y+len);
    }
    ctx.stroke();
    // dot at end
    ctx.fillStyle = pal.accent;
    ctx.shadowBlur = 8;
    ctx.beginPath();
    const ex = dir===0? x+len : x + 20*(rand()>0.5?1:-1);
    const ey = dir===0? y + 20*(rand()>0.5?1:-1) : y+len;
    ctx.arc(ex, ey, 2, 0, Math.PI*2);
    ctx.fill();
  }
  ctx.restore();
}

// Corner bracket
function cornerBracket(x,y,size,color,flip=false) {
  const s = size;
  ctx.save();
  ctx.strokeStyle = color;
  ctx.lineWidth = 2;
  ctx.shadowColor = color;
  ctx.shadowBlur = 6;
  ctx.beginPath();
  if(!flip) {
    ctx.moveTo(x, y+s); ctx.lineTo(x,y); ctx.lineTo(x+s,y);
  } else {
    ctx.moveTo(x-s, y); ctx.lineTo(x,y); ctx.lineTo(x,y+s);
  }
  ctx.stroke();
  ctx.restore();
}

// =============================================
// LAYOUTS
// =============================================

function drawFull(pal, rand, cfg) {
  const W=1280, H=720;
  const ac = cfg.accent || pal.accent;

  // Background
  const bgGrad = ctx.createLinearGradient(0,0,W,H);
  bgGrad.addColorStop(0, pal.bg1);
  bgGrad.addColorStop(1, pal.bg2);
  ctx.fillStyle = bgGrad;
  ctx.fillRect(0,0,W,H);

  drawHexBg(pal, rand);
  drawCircuitLines(pal, rand);

  // Side ambient
  const sideGrad = ctx.createRadialGradient(W,0,0,W,0,500);
  sideGrad.addColorStop(0, hexToRgba(ac, 0.15));
  sideGrad.addColorStop(1, 'transparent');
  ctx.fillStyle = sideGrad;
  ctx.fillRect(0,0,W,H);

  // Top bar
  const topGrad = ctx.createLinearGradient(0,0,W,0);
  topGrad.addColorStop(0, hexToRgba(ac,0.12));
  topGrad.addColorStop(0.5, hexToRgba(ac,0.04));
  topGrad.addColorStop(1, hexToRgba(pal.accent2, 0.15));
  ctx.fillStyle = topGrad;
  ctx.fillRect(0, 0, W, 40);
  glowLine(0, 40, W, 40, ac, 1.5, 10);

  // Platform logo text
  ctx.save();
  ctx.font = `bold 11px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 8;
  ctx.fillText('◉ LIVE', 20, 26);
  ctx.shadowBlur = 0;
  ctx.fillStyle = pal.text;
  ctx.fillText(cfg.channel.toUpperCase(), 70, 26);

  // Social icons row (right)
  const socials = cfg.platform==='twitch'
    ? ['TWITCH','YOUTUBE','INSTAGRAM','TWITTER']
    : ['YOUTUBE','TWITCH','INSTAGRAM','TWITTER'];
  let sx = W - 20;
  socials.reverse().forEach(s => {
    ctx.fillStyle = hexToRgba(ac, 0.7);
    ctx.fillText(s, sx - ctx.measureText(s).width, 26);
    sx -= ctx.measureText(s).width + 20;
    glowLine(sx+10, 16, sx+10, 32, hexToRgba(ac,0.3), 1, 0);
  });
  ctx.restore();

  // MAIN SCREEN
  const mX=30, mY=50, mW=680, mH=430;
  // Glow behind screen
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 40;
  roundRect(mX-4, mY-4, mW+8, mH+8, 6, hexToRgba(ac,0.04), ac, 1);
  ctx.restore();

  // Screen fill
  roundRect(mX, mY, mW, mH, 4, '#000000', null);

  // Scanlines on screen
  ctx.save();
  ctx.globalAlpha = 0.04;
  for(let y=mY;y<mY+mH;y+=4) {
    ctx.fillStyle = '#ffffff';
    ctx.fillRect(mX,y,mW,2);
  }
  ctx.restore();

  // Screen corner brackets
  cornerBracket(mX, mY, 20, ac);
  cornerBracket(mX+mW, mY, 20, ac, true);
  cornerBracket(mX, mY+mH, 20, ac);

  // Screen label
  ctx.save();
  ctx.font = `bold 10px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 6;
  ctx.fillText('MAIN DISPLAY', mX+8, mY+mH-8);
  ctx.restore();

  // CHAT PANEL
  const cX=730, cY=50, cW=200, cH=300;
  roundRect(cX,cY,cW,cH,4, hexToRgba(pal.panel,0.9), ac, 1.5);
  cornerBracket(cX,cY,14,ac);
  cornerBracket(cX+cW,cY,14,ac,true);

  ctx.save();
  ctx.font = `600 10px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 8;
  ctx.fillText(cfg.channel.toUpperCase(), cX+12, cY+20);
  ctx.fillStyle = hexToRgba(pal.text,0.5);
  ctx.shadowBlur = 0;
  ctx.fillText('JOIN TO CHAT ▶', cX+12, cY+36);
  ctx.restore();

  // Chat lines
  const chatColors = [ac, '#ff8866', '#88ffaa', '#ffcc44', '#cc88ff'];
  for(let i=0;i<5;i++) {
    const cy2 = cY + 55 + i*42;
    const bw = 30 + rand()*60;
    ctx.save();
    ctx.globalAlpha = 0.25;
    roundRect(cX+12, cy2, bw, 8, 4, chatColors[i%chatColors.length]);
    ctx.globalAlpha = 0.12;
    roundRect(cX+12, cy2+12, bw + rand()*40, 6, 3, pal.text);
    roundRect(cX+12, cy2+22, bw + rand()*20 - 10, 6, 3, pal.text);
    ctx.restore();
  }

  // CAM PANEL
  const camX=940, camY=50, camW=310, camH=195;
  roundRect(camX,camY,camW,camH,4, '#000', ac, 1.5);
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 20;
  roundRect(camX,camY,camW,camH,4, null, ac, 1.5);
  ctx.restore();
  cornerBracket(camX,camY,16,ac);
  cornerBracket(camX+camW,camY,16,ac,true);

  // Cam scanlines
  ctx.save();
  ctx.globalAlpha = 0.03;
  for(let y=camY;y<camY+camH;y+=3) {
    ctx.fillStyle = '#fff';
    ctx.fillRect(camX,y,camW,1);
  }
  ctx.restore();

  ctx.save();
  ctx.font = `bold 11px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 8;
  ctx.fillText('◉ CAM', camX + camW - ctx.measureText('◉ CAM').width - 10, camY+20);
  ctx.fillText(cfg.channel.toUpperCase(), camX+10, camY+camH-10);
  ctx.restore();

  // INFO PANELS (right side)
  const btns = [
    { icon:'👤', top:'MORE INFO', label:'ABOUT ME', color: ac },
    { icon:'📷', top:`CHECK OUT MY`, label: cfg.platform==='youtube'?'YOUTUBE':'INSTAGRAM', color: ac },
    { icon:'🐦', top:'FOLLOW ME ON', label:'TWITTER', color: ac },
  ];
  btns.forEach((b,i) => {
    const bX = 940, bY = 258 + i*86, bW=310, bH=72;
    // bg
    const bGrad = ctx.createLinearGradient(bX,bY,bX+bW,bY);
    bGrad.addColorStop(0, hexToRgba(pal.panel,0.95));
    bGrad.addColorStop(1, hexToRgba(b.color,0.15));
    roundRect(bX,bY,bW,bH,4, bGrad, b.color, 1.5);

    // Icon square
    const igGrad = ctx.createLinearGradient(bX,bY,bX+72,bY+bH);
    igGrad.addColorStop(0, hexToRgba(b.color,0.25));
    igGrad.addColorStop(1, hexToRgba(b.color,0.1));
    roundRect(bX,bY,72,bH,4, igGrad, b.color, 1);
    ctx.save();
    ctx.font = '28px serif';
    ctx.fillText(b.icon, bX+22, bY+44);
    ctx.restore();

    // Text
    ctx.save();
    ctx.font = `500 10px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(pal.text,0.7);
    ctx.fillText(b.top, bX+84, bY+26);
    ctx.font = `900 22px 'Rajdhani'`;
    ctx.fillStyle = pal.text;
    ctx.shadowColor = b.color;
    ctx.shadowBlur = 6;
    ctx.fillText(b.label, bX+84, bY+52);
    ctx.restore();

    // Right accent bar
    ctx.save();
    ctx.fillStyle = b.color;
    ctx.shadowColor = b.color;
    ctx.shadowBlur = 10;
    ctx.fillRect(bX+bW-4, bY+10, 4, bH-20);
    ctx.restore();
  });

  // Bottom events bar
  const evY = 492;
  const bGrad = ctx.createLinearGradient(0,evY,W,evY);
  bGrad.addColorStop(0, hexToRgba(pal.panel,0.95));
  bGrad.addColorStop(1, hexToRgba(pal.panel,0.7));
  roundRect(30, evY, 890, 42, 3, bGrad, hexToRgba(ac,0.3), 1);
  glowLine(30, evY, 920, evY, ac, 1, 5);

  const events = [
    {icon:'💰', sub:'NEW DONATION', val:''},
    {icon:'👤', sub:'NEW FOLLOWER', val:''},
    {icon:'⭐', sub:'NEW SUBSCRIBER', val:''},
    {icon:'🏆', sub:'TOP DONATION', val:''},
  ];
  events.forEach((ev, i) => {
    const ex = 50 + i*222;
    ctx.save();
    ctx.font = `500 9px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(pal.text,0.6);
    ctx.fillText(ev.icon+' '+ev.sub, ex, evY+16);
    ctx.globalAlpha = 0.15;
    roundRect(ex, evY+20, 170, 10, 3, ac);
    ctx.restore();
  });

  // Bottom screens (OFFLINE/ENDING/STARTING)
  const screens = [
    { label:'OFFLINE', x:30, y:548 },
    { label:'ENDING', x:336, y:548 },
    { label:'STARTING', x:642, y:548 },
  ];
  screens.forEach(s => {
    const sW=300, sH=162;
    const sGrad = ctx.createLinearGradient(s.x,s.y,s.x+sW,s.y+sH);
    sGrad.addColorStop(0, hexToRgba(pal.bg2,0.9));
    sGrad.addColorStop(1, hexToRgba(ac,0.1));
    roundRect(s.x,s.y,sW,sH,6, sGrad, ac, 1.5);

    // Abstract shape
    ctx.save();
    ctx.globalAlpha = 0.18;
    const shGrad = ctx.createRadialGradient(s.x+200, s.y+sH, 0, s.x+200, s.y+sH, 120);
    shGrad.addColorStop(0, ac);
    shGrad.addColorStop(1, 'transparent');
    ctx.fillStyle = shGrad;
    ctx.beginPath();
    ctx.moveTo(s.x+sW-30, s.y+sH-10);
    ctx.lineTo(s.x+sW-10, s.y+sH/2);
    ctx.lineTo(s.x+sW*0.6, s.y+10);
    ctx.lineTo(s.x+sW*0.3, s.y+sH*0.3);
    ctx.closePath();
    ctx.fill();
    ctx.restore();

    cornerBracket(s.x+4,s.y+4,12,ac);

    ctx.save();
    ctx.font = `600 9px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(ac,0.8);
    ctx.fillText('STREAM IS', s.x+14, s.y+28);
    ctx.font = `900 30px 'Rajdhani'`;
    ctx.fillStyle = pal.text;
    ctx.shadowColor = ac;
    ctx.shadowBlur = 12;
    ctx.letterSpacing = '2px';
    ctx.fillText(s.label, s.x+14, s.y+65);
    ctx.font = `500 9px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(pal.text,0.5);
    ctx.shadowBlur = 0;
    ctx.fillText(cfg.channel.toUpperCase(), s.x+14, s.y+sH-12);
    ctx.restore();
  });

  // Watermark
  ctx.save();
  ctx.font = `italic 600 14px 'Exo 2'`;
  ctx.fillStyle = hexToRgba(pal.text,0.2);
  ctx.fillText('StreamForge', W-110, H-12);
  ctx.restore();
}

// =============================================
function drawMinimal(pal, rand, cfg) {
  const W=1280, H=720;
  const ac = cfg.accent || pal.accent;

  ctx.fillStyle = pal.bg1;
  ctx.fillRect(0,0,W,H);

  // Subtle diagonal stripe
  ctx.save();
  ctx.globalAlpha = 0.04;
  for(let i=-20;i<60;i++) {
    ctx.strokeStyle = ac;
    ctx.lineWidth = 1;
    ctx.beginPath();
    ctx.moveTo(i*30-H, 0);
    ctx.lineTo(i*30, H);
    ctx.stroke();
  }
  ctx.restore();

  // Radial center glow
  const rg = ctx.createRadialGradient(W/2,H/2,0,W/2,H/2,600);
  rg.addColorStop(0, hexToRgba(ac,0.06));
  rg.addColorStop(1,'transparent');
  ctx.fillStyle = rg;
  ctx.fillRect(0,0,W,H);

  // Top thin bar
  const tg = ctx.createLinearGradient(0,0,W,0);
  tg.addColorStop(0,'transparent');
  tg.addColorStop(0.5, hexToRgba(ac,0.8));
  tg.addColorStop(1,'transparent');
  ctx.fillStyle = tg;
  ctx.fillRect(0,0,W,2);

  // Main screen
  const mX=50, mY=60, mW=740, mH=460;
  roundRect(mX,mY,mW,mH,2, '#000', ac, 1);
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 30;
  roundRect(mX,mY,mW,mH,2, null, ac, 0.5);
  ctx.restore();

  // Thin corner accents
  [[mX,mY],[mX+mW,mY],[mX,mY+mH],[mX+mW,mY+mH]].forEach(([cx,cy],i) => {
    const d = 16;
    ctx.save();
    ctx.strokeStyle = ac;
    ctx.lineWidth = 2;
    ctx.shadowColor = ac;
    ctx.shadowBlur = 8;
    ctx.beginPath();
    if(i===0){ctx.moveTo(cx,cy+d);ctx.lineTo(cx,cy);ctx.lineTo(cx+d,cy);}
    if(i===1){ctx.moveTo(cx-d,cy);ctx.lineTo(cx,cy);ctx.lineTo(cx,cy+d);}
    if(i===2){ctx.moveTo(cx,cy-d);ctx.lineTo(cx,cy);ctx.lineTo(cx+d,cy);}
    if(i===3){ctx.moveTo(cx-d,cy);ctx.lineTo(cx,cy);ctx.lineTo(cx,cy-d);}
    ctx.stroke();
    ctx.restore();
  });

  // Channel name — large
  ctx.save();
  ctx.font = `900 42px 'Rajdhani'`;
  ctx.fillStyle = pal.text;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 20;
  ctx.fillText(cfg.channel.toUpperCase(), 820, 120);
  ctx.font = `600 12px 'Share Tech Mono'`;
  ctx.fillStyle = hexToRgba(ac,0.9);
  ctx.shadowBlur = 10;
  ctx.fillText('▶ '+cfg.tagline.toUpperCase(), 820, 148);
  ctx.restore();

  glowLine(820, 158, 820+300, 158, ac, 1, 4);

  // Stats boxes
  const stats = ['FOLLOWERS','SUBSCRIBERS','DONATIONS'];
  stats.forEach((s,i) => {
    const bX=820, bY=170+i*68, bW=420, bH=56;
    const bg = ctx.createLinearGradient(bX,bY,bX+bW,bY);
    bg.addColorStop(0, hexToRgba(pal.panel,0.9));
    bg.addColorStop(1, hexToRgba(ac,0.05));
    roundRect(bX,bY,bW,bH,3, bg, hexToRgba(ac,0.3), 1);
    ctx.save();
    ctx.font = `500 10px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(pal.text,0.5);
    ctx.fillText(s, bX+16, bY+20);
    ctx.font = `700 16px 'Exo 2'`;
    ctx.fillStyle = hexToRgba(ac,0.9);
    ctx.fillText('—', bX+16, bY+42);
    // progress bar
    ctx.globalAlpha = 0.15;
    roundRect(bX+100, bY+30, 280, 6, 3, ac);
    ctx.restore();
    // left accent
    ctx.save();
    ctx.fillStyle = ac;
    ctx.shadowColor = ac;
    ctx.shadowBlur = 8;
    ctx.fillRect(bX, bY+8, 3, bH-16);
    ctx.restore();
  });

  // Bottom info
  ctx.save();
  ctx.font = `600 11px 'Share Tech Mono'`;
  ctx.fillStyle = hexToRgba(ac,0.7);
  ctx.fillText(cfg.social, 820, 400);
  ctx.restore();

  // Bottom bar
  const evY = 560;
  const evGrad = ctx.createLinearGradient(0,evY,W,evY);
  evGrad.addColorStop(0, hexToRgba(pal.panel,0.8));
  evGrad.addColorStop(1, hexToRgba(pal.panel,0.4));
  roundRect(50, evY, W-100, 50, 3, evGrad, hexToRgba(ac,0.2), 1);
  glowLine(50, evY, W-50, evY, ac, 1, 4);

  const evItems = ['NEW FOLLOWER','NEW SUBSCRIBER','TOP DONATION','RECENT CHEER'];
  evItems.forEach((ev,i) => {
    const ex = 70 + i*295;
    ctx.save();
    ctx.font = `500 10px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(ac,0.6);
    ctx.fillText(ev, ex, evY+22);
    ctx.globalAlpha = 0.1;
    roundRect(ex, evY+28, 240, 8, 4, pal.text);
    ctx.restore();
  });

  ctx.save();
  ctx.font = `italic 600 13px 'Exo 2'`;
  ctx.fillStyle = hexToRgba(pal.text,0.15);
  ctx.fillText('StreamForge', W-110, H-10);
  ctx.restore();
}

// =============================================
function drawPanels(pal, rand, cfg) {
  const W=1280, H=720;
  const ac = cfg.accent || pal.accent;

  const bg = ctx.createLinearGradient(0,0,W,H);
  bg.addColorStop(0, pal.bg1);
  bg.addColorStop(1, pal.bg2);
  ctx.fillStyle = bg;
  ctx.fillRect(0,0,W,H);

  drawHexBg(pal, rand);

  // Corner radial glows
  [{x:0,y:0},{x:W,y:H}].forEach(({x,y}) => {
    const rg = ctx.createRadialGradient(x,y,0,x,y,400);
    rg.addColorStop(0, hexToRgba(ac,0.12));
    rg.addColorStop(1,'transparent');
    ctx.fillStyle = rg;
    ctx.fillRect(0,0,W,H);
  });

  // Header
  const hGrad = ctx.createLinearGradient(0,0,W,0);
  hGrad.addColorStop(0, hexToRgba(ac,0.25));
  hGrad.addColorStop(0.5, hexToRgba(ac,0.06));
  hGrad.addColorStop(1, hexToRgba(pal.accent2,0.2));
  ctx.fillStyle = hGrad;
  ctx.fillRect(0,0,W,52);
  glowLine(0,52,W,52,ac,1.5,12);

  ctx.save();
  ctx.font = `900 20px 'Rajdhani'`;
  ctx.fillStyle = pal.text;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 12;
  ctx.fillText(cfg.channel.toUpperCase(), 20, 34);
  ctx.font = `600 11px 'Share Tech Mono'`;
  ctx.fillStyle = hexToRgba(ac,0.8);
  ctx.shadowBlur = 6;
  ctx.fillText('◉ ' + cfg.tagline.toUpperCase(), 20, 48);
  ctx.restore();

  // RIGHT: channel info panels
  const panels = [
    { title:'ABOUT', icon:'👤', text:cfg.channel },
    { title:'INSTAGRAM', icon:'📷', text:cfg.social },
    { title:'TWITTER', icon:'🐦', text:cfg.social },
    { title:'DISCORD', icon:'💬', text:cfg.social },
  ];
  panels.forEach((p,i) => {
    const pX=960, pY=60+i*80, pW=310, pH=68;
    const pGrad = ctx.createLinearGradient(pX,pY,pX+pW,pY+pH);
    pGrad.addColorStop(0, hexToRgba(pal.panel,0.98));
    pGrad.addColorStop(1, hexToRgba(ac,0.08));
    roundRect(pX,pY,pW,pH,4, pGrad, ac, 1.5);
    ctx.save();
    ctx.shadowColor = ac;
    ctx.shadowBlur = 15;
    roundRect(pX,pY,pW,pH,4, null, ac, 0.5);
    ctx.restore();

    roundRect(pX,pY,66,pH,4, hexToRgba(ac,0.15), ac, 1);
    ctx.save();
    ctx.font = '26px serif';
    ctx.fillText(p.icon, pX+18, pY+44);
    ctx.font = `600 9px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(pal.text,0.5);
    ctx.fillText(p.title, pX+78, pY+24);
    ctx.font = `700 16px 'Exo 2'`;
    ctx.fillStyle = pal.text;
    ctx.shadowColor = ac;
    ctx.shadowBlur = 6;
    ctx.fillText(p.text, pX+78, pY+46);
    ctx.restore();
  });

  // Center cam panel
  const camX=530, camY=60, camW=420, camH=290;
  roundRect(camX,camY,camW,camH,6, '#000', ac, 2);
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 40;
  roundRect(camX,camY,camW,camH,6, null, ac, 0.5);
  ctx.restore();
  ctx.save();
  ctx.font = `600 11px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 8;
  ctx.fillText('◉ WEBCAM', camX+12, camY+22);
  ctx.restore();
  cornerBracket(camX+4,camY+4,16,ac);
  cornerBracket(camX+camW-4,camY+4,16,ac,true);

  // Main screen
  const mX=30, mY=60, mW=492, mH=380;
  roundRect(mX,mY,mW,mH,6, '#000', ac, 2);
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 30;
  roundRect(mX,mY,mW,mH,6, null, ac, 0.5);
  ctx.restore();
  ctx.save();
  ctx.font = `600 11px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 8;
  ctx.fillText('◉ GAME FEED', mX+12, mY+22);
  ctx.restore();
  cornerBracket(mX+4,mY+4,16,ac);
  cornerBracket(mX+mW-4,mY+4,16,ac,true);

  // Bottom
  const btmY = 456;
  ['NEW FOLLOWER','NEW SUBSCRIBER','TOP DONATION','RECENT HYPE'].forEach((ev,i) => {
    const bX = 30+i*298, bW=280, bH=50;
    roundRect(bX, btmY, bW, bH, 4, hexToRgba(pal.panel,0.9), hexToRgba(ac,0.4), 1);
    glowLine(bX, btmY, bX+bW, btmY, ac, 1, 4);
    ctx.save();
    ctx.font = `600 10px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(ac,0.7);
    ctx.fillText(ev, bX+12, btmY+20);
    ctx.globalAlpha = 0.12;
    roundRect(bX+12, btmY+28, 200, 10, 5, ac);
    ctx.restore();
  });

  // OFFLINE/STARTING/ENDING row
  ['OFFLINE','STARTING','ENDING'].forEach((label,i) => {
    const sX=30+i*300, sY=518, sW=280, sH=188;
    const sg = ctx.createLinearGradient(sX,sY,sX+sW,sY+sH);
    sg.addColorStop(0, hexToRgba(pal.bg2,0.97));
    sg.addColorStop(1, hexToRgba(ac,0.12));
    roundRect(sX,sY,sW,sH,6, sg, ac, 1.5);

    ctx.save();
    ctx.shadowColor = ac;
    ctx.shadowBlur = 20;
    const shGrad = ctx.createRadialGradient(sX+sW, sY+sH, 0, sX+sW, sY+sH, 150);
    shGrad.addColorStop(0, hexToRgba(ac,0.2));
    shGrad.addColorStop(1,'transparent');
    ctx.fillStyle = shGrad;
    ctx.fillRect(sX, sY, sW, sH);
    ctx.restore();

    cornerBracket(sX+4,sY+4,12,ac);
    ctx.save();
    ctx.font = `600 9px 'Share Tech Mono'`;
    ctx.fillStyle = hexToRgba(ac,0.8);
    ctx.fillText('STREAM IS', sX+14, sY+28);
    ctx.font = `900 32px 'Rajdhani'`;
    ctx.fillStyle = pal.text;
    ctx.shadowColor = ac;
    ctx.shadowBlur = 15;
    ctx.fillText(label, sX+14, sY+70);
    ctx.restore();
  });

  ctx.save();
  ctx.font = `italic 600 13px 'Exo 2'`;
  ctx.fillStyle = hexToRgba(pal.text,0.15);
  ctx.fillText('StreamForge', W-110, H-10);
  ctx.restore();
}

// =============================================
function drawScreens(pal, rand, cfg) {
  const W=1280, H=720;
  const ac = cfg.accent || pal.accent;

  ctx.fillStyle = pal.bg1;
  ctx.fillRect(0,0,W,H);
  drawCircuitLines(pal,rand);

  // Big ambient
  const aGrad = ctx.createRadialGradient(W*0.7,H*0.3,0,W*0.7,H*0.3,700);
  aGrad.addColorStop(0, hexToRgba(ac,0.1));
  aGrad.addColorStop(1,'transparent');
  ctx.fillStyle = aGrad;
  ctx.fillRect(0,0,W,H);

  // Top title
  glowLine(0,70,W,70,ac,1,8);
  ctx.save();
  ctx.font = `900 36px 'Rajdhani'`;
  ctx.fillStyle = pal.text;
  ctx.shadowColor = ac;
  ctx.shadowBlur = 20;
  ctx.fillText(cfg.channel.toUpperCase(), 30, 50);
  ctx.font = `600 12px 'Share Tech Mono'`;
  ctx.fillStyle = hexToRgba(ac,0.8);
  ctx.shadowBlur = 8;
  ctx.fillText('◉ '+cfg.tagline+' | '+cfg.social, 30, 66);
  ctx.restore();

  // Large main screen
  const mX=30, mY=84, mW=820, mH=520;
  roundRect(mX,mY,mW,mH,6, '#000', ac, 2);
  ctx.save();
  ctx.shadowColor = ac;
  ctx.shadowBlur = 50;
  roundRect(mX,mY,mW,mH,6, null, ac, 0.5);
  ctx.restore();

  // Scanlines
  ctx.save();
  ctx.globalAlpha = 0.03;
  for(let y=mY;y<mY+mH;y+=4){ctx.fillStyle='#fff';ctx.fillRect(mX,y,mW,2);}
  ctx.restore();

  cornerBracket(mX+6,mY+6,20,ac);
  cornerBracket(mX+mW-6,mY+6,20,ac,true);
  cornerBracket(mX+6,mY+mH-6,20,ac);
  cornerBracket(mX+mW-6,mY+mH-6,20,ac,true);

  ctx.save();
  ctx.font = `600 11px 'Share Tech Mono'`;
  ctx.fillStyle = ac;
  ctx.shadowColor = ac; ctx.shadowBlur = 8;
  ctx.fillText('◉ LIVE STREAM', mX+14, mY+22);
  ctx.fillText('REC', mX+mW-50, mY+22);
  // Blinking dot
  ctx.fillStyle = '#ff3366';
  ctx.shadowColor = '#ff3366'; ctx.shadowBlur = 10;
  ctx.beginPath(); ctx.arc(mX+mW-60, mY+18, 4, 0, Math.PI*2); ctx.fill();
  ctx.restore();

  // Right side stacked panels
  const rX=870, panW=390;
  // Cam
  const camH=220;
  roundRect(rX,mY,panW,camH,6,'#000',ac,2);
  ctx.save();
  ctx.shadowColor=ac;ctx.shadowBlur=25;
  roundRect(rX,mY,panW,camH,6,null,ac,0.5);
  ctx.restore();
  cornerBracket(rX+4,mY+4,14,ac);
  cornerBracket(rX+panW-4,mY+4,14,ac,true);
  ctx.save();
  ctx.font=`600 11px 'Share Tech Mono'`;
  ctx.fillStyle=ac;ctx.shadowColor=ac;ctx.shadowBlur=8;
  ctx.fillText('◉ CAM VIEW', rX+12,mY+22);
  ctx.fillText(cfg.channel.toUpperCase(), rX+12, mY+camH-10);
  ctx.restore();

  // Chat
  const chatY=mY+camH+10, chatH=mH-camH-10;
  roundRect(rX,chatY,panW,chatH,6,hexToRgba(pal.panel,0.9),ac,1.5);
  ctx.save();
  ctx.font=`600 11px 'Share Tech Mono'`;
  ctx.fillStyle=ac;ctx.shadowColor=ac;ctx.shadowBlur=8;
  ctx.fillText('CHAT', rX+12,chatY+22);
  ctx.fillStyle=hexToRgba(pal.text,0.5);ctx.shadowBlur=0;
  ctx.fillText('JOIN TO CHAT ▶',rX+12,chatY+38);
  ctx.restore();

  // Chat lines
  const chatColors2=[ac,'#ff8866','#88ffaa','#ffcc44','#cc88ff','#ff66bb'];
  for(let i=0;i<8;i++){
    const cy=chatY+55+i*36;
    ctx.save();
    ctx.globalAlpha=0.3;
    roundRect(rX+12,cy,30+rand()*50,7,4,chatColors2[i%chatColors2.length]);
    ctx.globalAlpha=0.12;
    roundRect(rX+12,cy+11,60+rand()*200,5,3,pal.text);
    ctx.restore();
  }

  // Watermark
  ctx.save();
  ctx.font=`italic 600 13px 'Exo 2'`;
  ctx.fillStyle=hexToRgba(pal.text,0.15);
  ctx.fillText('StreamForge',W-110,H-10);
  ctx.restore();
}

// =============================================
// MAIN GENERATE
// =============================================
function generateOverlay() {
  state.seed = Math.random();
  const rand = seededRand(Math.floor(state.seed * 999999));
  const pal = themes[state.theme];
  const cfg = {
    channel: document.getElementById('channelName').value || 'YourChannel',
    tagline: document.getElementById('tagline').value || 'LIVE GAMING',
    social: document.getElementById('social').value || '@yourchannel',
    platform: state.platform,
    accent: state.accentColor,
  };

  ctx.clearRect(0,0,1280,720);

  const layouts = { full: drawFull, minimal: drawMinimal, panels: drawPanels, screens: drawScreens };
  (layouts[state.layout] || drawFull)(pal, rand, cfg);
}

function downloadOverlay() {
  const link = document.createElement('a');
  link.download = `overlay_${state.theme}_${state.layout}.png`;
  link.href = canvas.toDataURL('image/png');
  link.click();
}

// =============================================
// EVENT LISTENERS
// =============================================
document.querySelectorAll('.theme-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.theme-btn').forEach(b=>b.classList.remove('active'));
    btn.classList.add('active');
    state.theme = btn.dataset.theme;
    // Reset accent to theme default if not custom
    const pal = themes[state.theme];
    state.accentColor = pal.accent;
    generateOverlay();
  });
});

document.querySelectorAll('#layoutRow .var-chip').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('#layoutRow .var-chip').forEach(b=>b.classList.remove('active'));
    btn.classList.add('active');
    state.layout = btn.dataset.layout;
    generateOverlay();
  });
});

document.querySelectorAll('.swatch').forEach(sw => {
  sw.addEventListener('click', () => {
    document.querySelectorAll('.swatch').forEach(s=>s.classList.remove('active'));
    sw.classList.add('active');
    state.accentColor = sw.dataset.color;
    document.getElementById('customColor').value = sw.dataset.color;
    generateOverlay();
  });
});

document.getElementById('customColor').addEventListener('input', e => {
  state.accentColor = e.target.value;
  document.querySelectorAll('.swatch').forEach(s=>s.classList.remove('active'));
  generateOverlay();
});

document.querySelectorAll('#platformGroup .toggle-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('#platformGroup .toggle-btn').forEach(b=>b.classList.remove('active'));
    btn.classList.add('active');
    state.platform = btn.dataset.platform;
    generateOverlay();
  });
});

['channelName','tagline','social'].forEach(id => {
  document.getElementById(id).addEventListener('input', () => generateOverlay());
});

// Generate on load
generateOverlay();
</script>
</body>
</html>
