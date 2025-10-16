<!doctype html>
<html lang="ar">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Animated Elegant Robot — Sample</title>
  <style>
    :root{
      --bg:#0b0f1a;
      --card:#0f1724;
      --accent:#6c5ce7; /* purple */
      --accent-2:#00d4ff; /* cyan */
      --glass: rgba(255,255,255,0.06);
    }
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Arial;color:#e6eef8;background:linear-gradient(180deg,var(--bg),#061021);display:grid;place-items:center}
    .wrap{width:480px;max-width:94vw;padding:28px;border-radius:18px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));box-shadow:0 10px 30px rgba(2,6,23,0.7);backdrop-filter: blur(6px);}
    .header{display:flex;align-items:center;gap:14px;margin-bottom:18px}
    .title{font-size:18px;font-weight:600}
    .subtitle{font-size:13px;color:#9fb3d6}

    /* Robot stage */
    .stage{display:flex;justify-content:center;padding:16px}
    .robot{width:260px;height:320px;position:relative;transform-origin:center;animation:float 3.6s ease-in-out infinite}

    @keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-8px)}100%{transform:translateY(0)}}

    /* SVG sizing */
    svg{width:100%;height:100%;display:block}

    /* breathing light */
    .glow{filter:drop-shadow(0 6px 18px rgba(108,92,231,0.28));}

    /* eye blink */
    .eye-clip rect{animation:blink 4s steps(2,end) infinite}
    @keyframes blink{0%,6%,100%{transform:scaleY(0)}7%,9%{transform:scaleY(1)}10%,94%{transform:scaleY(1)}95%,97%{transform:scaleY(0)}}

    /* antenna pulse */
    .antenna-dot{animation:antennaPulse 1.6s ease-in-out infinite}
    @keyframes antennaPulse{0%{transform:scale(0.85);opacity:0.85}50%{transform:scale(1.25);opacity:1}100%{transform:scale(0.85);opacity:0.85}}

    /* display text */
    .meta{display:flex;flex-direction:column;gap:6px;margin-top:12px}
    .meta .line{display:flex;justify-content:space-between;font-size:13px;color:#bcd3ee}
    .badge{padding:6px 10px;border-radius:999px;background:linear-gradient(90deg,var(--accent),var(--accent-2));font-weight:600;color:#041022}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="header">
      <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:grid;place-items:center;box-shadow:0 6px 20px rgba(0,0,0,0.45);">
        <svg width="34" height="34" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden>
          <path d="M12 2v4" stroke="#041022" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M8.5 7.2L7 9" stroke="#041022" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M15.5 7.2L17 9" stroke="#041022" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
          <rect x="4" y="9" width="16" height="11" rx="2.4" fill="#041022" opacity="0.06"/>
        </svg>
      </div>
      <div>
        <div class="title">Salsabeel — Aspiring AI Founder</div>
        <div class="subtitle">Python • AI • Machine Learning • Future CEO</div>
      </div>
      <div style="margin-left:auto">
        <div class="badge">Elegant Robot</div>
      </div>
    </div>

    <div class="stage">
      <!-- Animated robot SVG -->
      <div class="robot glow" role="img" aria-label="Animated elegant robot">
        <svg viewBox="0 0 240 300" xmlns="http://www.w3.org/2000/svg">
          <!-- shadow -->
          <ellipse cx="120" cy="282" rx="64" ry="8" fill="rgba(0,0,0,0.45)" />

          <!-- body -->
          <g transform="translate(20,36)">
            <rect x="20" y="48" rx="20" ry="20" width="180" height="160" fill="url(#bodyGrad)" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

            <!-- chest display -->
            <rect x="60" y="88" width="100" height="62" rx="10" fill="rgba(4,16,34,0.6)" />
            <g>
              <circle cx="110" cy="120" r="20" fill="#071427" stroke="rgba(255,255,255,0.04)"/>
              <circle cx="110" cy="120" r="10" fill="url(#eyeGrad)"/>
            </g>

            <!-- small lights -->
            <circle cx="46" cy="72" r="6" fill="rgba(255,255,255,0.04)" />
            <circle cx="194" cy="72" r="6" fill="rgba(255,255,255,0.04)" />

            <!-- neck -->
            <rect x="96" y="28" width="48" height="28" rx="8" fill="rgba(255,255,255,0.02)" />

            <!-- head -->
            <g transform="translate(44,0)">
              <rect x="36" y="0" width="120" height="72" rx="18" fill="url(#headGrad)" stroke="rgba(255,255,255,0.04)"/>

              <!-- antenna -->
              <g transform="translate(96,-10)">
                <rect x="0" y="0" width="4" height="16" rx="2" fill="#b8c7ff" opacity="0.9"/>
                <circle class="antenna-dot" cx="2" cy="0" r="6" fill="url(#antennaGrad)"/>
              </g>

              <!-- eye area with blink clip -->
              <g transform="translate(52,18)">
                <defs>
                  <clipPath id="eyeClip">
                    <rect x="0" y="0" width="32" height="16" rx="8" />
                  </clipPath>
                </defs>
                <rect x="0" y="0" width="32" height="16" rx="8" fill="#041427" opacity="0.45" />
                <g clip-path="url(#eyeClip)">
                  <rect x="0" y="0" width="32" height="16" rx="8" fill="url(#eyeGrad)"/>
                  <!-- blink overlay animated -->
                  <rect class="eye-clip" x="0" y="0" width="32" height="16" rx="8" fill="#041427" transform-origin="16 8" />
                </g>
              </g>

              <!-- mouth indicator -->
              <rect x="76" y="52" width="28" height="6" rx="3" fill="#0b6b8f" opacity="0.95" />
            </g>

            <!-- arms -->
            <g>
              <rect x="4" y="80" width="18" height="92" rx="8" fill="url(#armGrad)" transform-origin="13 82" style="transform: rotate(-8deg);animation:wave 3s ease-in-out infinite;" />
              <rect x="218" y="80" width="18" height="92" rx="8" fill="url(#armGrad)" transform-origin="227 82" style="transform: rotate(8deg);animation:wave2 3s ease-in-out infinite;" />
            </g>
          </g>

          <defs>
            <linearGradient id="bodyGrad" x1="0" x2="1">
              <stop offset="0%" stop-color="#071427" />
              <stop offset="100%" stop-color="#0c1630" />
            </linearGradient>
            <linearGradient id="headGrad" x1="0" x2="1">
              <stop offset="0%" stop-color="#101827" />
              <stop offset="100%" stop-color="#071427" />
            </linearGradient>
            <linearGradient id="eyeGrad" x1="0" x2="1">
              <stop offset="0%" stop-color="#6c5ce7" />
              <stop offset="100%" stop-color="#00d4ff" />
            </linearGradient>
            <linearGradient id="antennaGrad" x1="0" x2="1">
              <stop offset="0%" stop-color="#9fa8ff" />
              <stop offset="100%" stop-color="#00d4ff" />
            </linearGradient>
            <linearGradient id="armGrad" x1="0" x2="1">
              <stop offset="0%" stop-color="#0e2032" />
              <stop offset="100%" stop-color="#071427" />
            </linearGradient>
          </defs>

          <style>
            /* small keyframes inside SVG for arms and blink fallback */
            @keyframes wave{0%{transform:rotate(-10deg)}50%{transform:rotate(8deg)}100%{transform:rotate(-10deg)}}
            @keyframes wave2{0%{transform:rotate(10deg)}50%{transform:rotate(-6deg)}100%{transform:rotate(10deg)}}
          </style>
        </svg>
      </div>
    </div>

    <div class="meta">
      <div class="line"><span>Core</span><span>Python • ML • AI</span></div>
      <div class="line"><span>Vision</span><span>Founding an AI company</span></div>
      <div class="line"><span>Try</span><span>Open this file in browser (double-click)</span></div>
    </div>
  </div>
</body>
</html>
