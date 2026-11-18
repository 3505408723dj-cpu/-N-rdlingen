<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Nördlingen 诺德林根 · 陨石之城 空间信息可视化</title>
<link rel="stylesheet" href="style.css" />
</head>
<body>

<!-- ============ D0 加载页 ============ -->
<div id="loading">
  <div class="meteor"></div>
  <h1 id="loading-title">一座建在陨石上的城市</h1>
  <p id="loading-sub">Nördlingen · 从 1450 万年前的撞击，到中世纪的城墙</p>
  <span class="hint" id="loading-hint">点击任意位置进入</span>
</div>

<!-- ============ 顶栏 ============ -->
<header id="header">
  <div class="brand" id="brand">
    <span class="brand-en">Nördlingen</span>
    <span class="brand-cn">诺德林根</span>
  </div>
  <div class="view-toggle" role="tablist">
    <button id="btn3d" class="active">3D 俯瞰</button>
    <button id="btn2d">2D 平面</button>
  </div>
  <div class="presets" id="presets">
    <button data-preset="1">① 陨石之眼</button>
    <button data-preset="2">② 中世纪防御</button>
    <button data-preset="3">③ 1634 战役</button>
    <button data-preset="4">④ 今日诺德林根</button>
  </div>
  <div class="header-actions">
    <button id="btn-data" class="ghost">数据</button>
    <button id="btn-autoplay" class="ghost" aria-pressed="false">自动播放</button>
  </div>
</header>

<!-- ============ 左侧图层控制台 ============ -->
<aside id="layer-panel">
  <div class="panel-title">图层控制台</div>
  <div class="mode-row">
    <button data-mode="free" class="active">自由</button>
    <button data-mode="single">单层</button>
    <button data-mode="compare">对比</button>
  </div>
  <div id="layer-list"></div>
  <div class="panel-hint" id="mode-hint"></div>
  <div class="panel-legend" id="panel-legend"></div>
</aside>

<!-- ============ 中央画布 ============ -->
<main id="canvas">
  <!-- 3D 俯瞰（Three.js 实时渲染） -->
  <div id="view-3d">
    <div id="scene-container"></div>
    <div id="hotspots"></div>
    <div id="wall-labels">
      <button class="wall-label" data-wall="main">主城墙 · 约 9.5 m</button>
      <button class="wall-label" data-wall="zwinger">外壕墙 Zwinger</button>
    </div>
    <div id="event-labels"></div>
    <div id="district-labels"></div>
    <div id="tour-labels"></div>
    <div id="focus-name" class="hidden"></div>
  </div>

  <!-- 2D 平面（实景俯视图 + 矢量标注） -->
  <div id="view-2d" class="hidden">
    <img id="map-photo" src="aerial.jpg" alt="Nördlingen 俯视图" />
    <svg id="map-svg" viewBox="0 0 1920 1080" preserveAspectRatio="xMidYMid meet" xmlns="http://www.w3.org/2000/svg"></svg>
  </div>

  <div id="hint-bar">左键<b>拖拽</b> 360° 环绕 · 点<b>建筑</b>放大 · <b>Daniel 塔</b>进入塔内 · <b>滚轮</b>缩放 · <b>← →</b> 时间轴 · <b>1/2</b> 视图 · <b>Esc</b> 返回</div>

  <!-- 演示视频录制：字幕卡 + 录制指示（默认隐藏，仅 ?record 模式启用） -->
  <div id="record-caption" class="hidden">
    <div class="rc-title" id="rc-title"></div>
    <div class="rc-sub" id="rc-sub"></div>
  </div>
  <div id="rec-badge" class="hidden"><span class="rec-dot"></span>REC <span id="rec-time">00:00</span></div>
</main>

<!-- ============ 详情浮层 ============ -->
<div id="detail-overlay" class="hidden">
  <button id="detail-close" aria-label="关闭">×</button>
  <div id="detail-tabs">
    <button data-tab="building" class="active">建筑</button>
    <button data-tab="layer">图层</button>
    <button data-tab="event">事件</button>
    <button data-tab="data">数据</button>
  </div>

  <!-- 建筑分析 -->
  <div id="tab-building" class="tab-panel">
    <div id="building-content"></div>
  </div>

  <!-- 图层科普 -->
  <div id="tab-layer" class="tab-panel hidden">
    <div id="layer-content"></div>
  </div>

  <!-- 事件概述 -->
  <div id="tab-event" class="tab-panel hidden">
    <div id="event-content"></div>
  </div>

  <!-- 数据图表 -->
  <div id="tab-data" class="tab-panel hidden">
    <h3>三级尺度</h3>
    <div class="scale-cards">
      <div class="scard"><div class="num">25 km</div><div class="lbl">陨石坑直径</div></div>
      <div class="scard"><div class="num">2.6 km</div><div class="lbl">城墙周长</div></div>
      <div class="scard"><div class="num">90 m</div><div class="lbl">Daniel 塔高</div></div>
    </div>
    <p class="note">坑 ≈ 城墙的 10 倍 ≈ 塔高的 280 倍</p>

    <h3>撞击参数</h3>
    <div class="impact-cards">
      <div class="icard"><div class="num">~1 km</div><div class="lbl">撞击体直径</div></div>
      <div class="icard"><div class="num">20–25 km/s</div><div class="lbl">撞击速度*</div></div>
      <div class="icard"><div class="num">1450 万年前</div><div class="lbl">形成年代</div></div>
      <div class="icard"><div class="num">Suevite</div><div class="lbl">撞击角砾岩</div></div>
    </div>

    <h3>人口变迁 <span class="mark">示意</span></h3>
    <svg viewBox="0 0 560 250" class="chart">
      <line x1="60" y1="210" x2="545" y2="210" stroke="#C7B99C"/>
      <line x1="60" y1="210" x2="60" y2="25" stroke="#C7B99C"/>
      <polyline points="60,142 156,134 252,168 348,151 444,134 540,40" fill="none" stroke="#C66B3D" stroke-width="2.5"/>
      <g fill="#C66B3D">
        <circle cx="60" cy="142" r="3.5"/><circle cx="156" cy="134" r="3.5"/><circle cx="252" cy="168" r="3.5"/>
        <circle cx="348" cy="151" r="3.5"/><circle cx="444" cy="134" r="3.5"/><circle cx="540" cy="40" r="3.5"/>
      </g>
      <g font-size="11" fill="#6F6553" text-anchor="middle">
        <text x="60" y="228">1300</text><text x="156" y="228">1600</text><text x="252" y="228">1634</text>
        <text x="348" y="228">1800</text><text x="444" y="228">1900</text><text x="540" y="228">2020</text>
      </g>
      <text x="60" y="128" font-size="11" fill="#37312A">0.8万</text>
      <text x="540" y="26" font-size="11" fill="#37312A">2万</text>
      <text x="252" y="160" font-size="10" fill="#B5442E">1634 战役人口锐减</text>
    </svg>

    <h3>功能分布 <span class="mark">示意</span></h3>
    <svg viewBox="0 0 560 60" class="chart bar">
      <rect x="20" y="10" width="264" height="30" fill="#C66B3D"/>
      <rect x="284" y="10" width="72" height="30" fill="#606C38"/>
      <rect x="356" y="10" width="72" height="30" fill="#C08E3A"/>
      <rect x="428" y="10" width="38" height="30" fill="#B3A18A"/>
      <rect x="466" y="10" width="74" height="30" fill="#4A7A7A"/>
    </svg>
    <ul class="legend-row">
      <li><i style="background:#C66B3D"></i>居住 55%</li>
      <li><i style="background:#606C38"></i>绿地 15%</li>
      <li><i style="background:#C08E3A"></i>商业 15%</li>
      <li><i style="background:#B3A18A"></i>宗教 8%</li>
      <li><i style="background:#4A7A7A"></i>市政 7%</li>
    </ul>
    <p class="note">* 撞击速度等为近似估算，标注「示意」项需在展板中注明。</p>
  </div>
</div>

<!-- ============ 塔内视点（Daniel 塔，拱窗） ============ -->
<div id="tower-view" class="hidden">
  <svg id="tower-frame-svg" viewBox="0 0 1440 900" preserveAspectRatio="none" aria-hidden="true">
    <defs>
      <!-- 石墙砌块（suevite 角砾岩：多色阶暖灰 + 细灰缝 + 受光高光） -->
      <pattern id="stonewall" width="128" height="56" patternUnits="userSpaceOnUse">
        <rect width="128" height="56" fill="#5f5749"/>
        <rect x="2" y="2" width="60" height="24" rx="1.5" fill="#8b7f6c"/>
        <rect x="65" y="2" width="61" height="24" rx="1.5" fill="#7b6f5d"/>
        <rect x="-28" y="30" width="60" height="24" rx="1.5" fill="#847866"/>
        <rect x="35" y="30" width="60" height="24" rx="1.5" fill="#756958"/>
        <rect x="98" y="30" width="61" height="24" rx="1.5" fill="#7f7462"/>
        <rect x="3" y="3" width="58" height="5" rx="2" fill="#a0937f" opacity=".6"/>
        <rect x="36" y="31" width="58" height="4" rx="2" fill="#978b77" opacity=".55"/>
        <rect x="3" y="21" width="58" height="3" rx="1.5" fill="#554c3e" opacity=".5"/>
        <rect x="36" y="49" width="58" height="3" rx="1.5" fill="#52493b" opacity=".5"/>
      </pattern>
      <!-- 墙面整体明暗（塔内昏暗，越靠边越暗） -->
      <radialGradient id="wall-shade" cx="50%" cy="46%" r="82%">
        <stop offset="0%" stop-color="#000" stop-opacity="0"/>
        <stop offset="50%" stop-color="#000" stop-opacity="0.12"/>
        <stop offset="100%" stop-color="#000" stop-opacity="0.5"/>
      </radialGradient>
      <!-- 窗外天光晕（窗洞周围被天光照亮） -->
      <radialGradient id="window-light" cx="50%" cy="76%" r="58%">
        <stop offset="0%" stop-color="#fff" stop-opacity="0.26"/>
        <stop offset="45%" stop-color="#fff" stop-opacity="0.06"/>
        <stop offset="100%" stop-color="#fff" stop-opacity="0"/>
      </radialGradient>
    </defs>

    <!-- 石墙 + 拱窗开口（开口比原版更大） -->
    <path fill="url(#stonewall)" fill-rule="evenodd" d="M0,0 H1440 V900 H0 Z M340,900 L340,660 A380,380 0 0 1 1100,660 L1100,900 Z"/>

    <!-- 窗外天光晕（照亮窗洞周围石墙） -->
    <rect width="1440" height="900" fill="url(#window-light)"/>

    <!-- 石墙整体光影 -->
    <rect width="1440" height="900" fill="url(#wall-shade)"/>

    <!-- 拱窗石质窗套（reveal，略凸出于墙面） -->
    <path fill="none" stroke="#4c4336" stroke-width="44" d="M340,660 A380,380 0 0 1 1100,660"/>
    <path fill="none" stroke="#4c4336" stroke-width="44" d="M340,678 L340,900 M1100,678 L1100,900"/>

    <!-- 窗套受光高光（朝外受天光） -->
    <path fill="none" stroke="#a2947f" stroke-width="7" d="M340,660 A380,380 0 0 1 1100,660"/>
    <path fill="none" stroke="#a2947f" stroke-width="7" d="M340,900 L340,678 M1100,900 L1100,678"/>

    <!-- 拱顶楔形石（voussoir）接缝 -->
    <path fill="none" stroke="#2b251d" stroke-width="4" stroke-dasharray="24 7" d="M340,660 A380,380 0 0 1 1100,660"/>
  </svg>
  <div id="tower-hint">透过 Daniel 塔拱窗 · 观测城镇一角　<b>拖拽</b>环视视角　<b>Esc</b> 返回全景</div>
</div>

<!-- ============ 底部时间轴 ============ -->
<footer id="timeline">
  <div class="time-title">历史时间轴</div>
  <div id="time-track">
    <div id="time-fill"></div>
    <div id="time-thumb"></div>
  </div>
  <div id="time-labels"></div>
  <div class="source-note">数据来源：Wikipedia · Nördlinger Ries / LDBV OpenData · OSM（规划书 §1 数据核实表）</div>
</footer>

<script src="three.min.js"></script>
<script src="script.js"></script>
</body>
</html>
