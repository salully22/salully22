### 🤖 Ambitious AI Dreamer

<p align="center">
  <svg width="180" height="180" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
    <!-- Body -->
    <rect x="60" y="70" width="80" height="60" rx="10" fill="#2f3542"/>
    <!-- Head -->
    <rect x="70" y="30" width="60" height="40" rx="8" fill="#57606f"/>
    <!-- Eyes -->
    <circle cx="85" cy="50" r="6" fill="#70a1ff">
      <animate attributeName="r" values="6;4;6" dur="1s" repeatCount="indefinite"/>
    </circle>
    <circle cx="115" cy="50" r="6" fill="#70a1ff">
      <animate attributeName="r" values="6;4;6" dur="1s" repeatCount="indefinite"/>
    </circle>
    <!-- Antenna -->
    <line x1="100" y1="30" x2="100" y2="15" stroke="#ced6e0" stroke-width="3"/>
    <circle cx="100" cy="12" r="4" fill="#ffa502">
      <animate attributeName="r" values="4;6;4" dur="1s" repeatCount="indefinite"/>
    </circle>
    <!-- Arms -->
    <line x1="60" y1="90" x2="40" y2="90" stroke="#747d8c" stroke-width="5">
      <animate attributeName="x2" values="40;35;40" dur="1s" repeatCount="indefinite"/>
    </line>
    <line x1="140" y1="90" x2="160" y2="90" stroke="#747d8c" stroke-width="5">
      <animate attributeName="x2" values="160;165;160" dur="1s" repeatCount="indefinite"/>
    </line>
    <!-- Text -->
    <text x="50%" y="160" text-anchor="middle" fill="#1e90ff" font-size="14" font-family="monospace">
      Building My AI Empire 💫
      <animate attributeName="opacity" values="1;0.4;1" dur="2s" repeatCount="indefinite"/>
    </text>
  </svg>
</p>

    }
    .robot {
      width: 250px;
      height: 300px;
      animation: float 3s ease-in-out infinite;
    }
    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    svg {
      width: 100%;
      height: 100%;
    }
    .antenna {
      animation: pulse 1.5s ease-in-out infinite;
      transform-origin: center;
    }
    @keyframes pulse {
      0% { transform: scale(0.8); opacity: 0.8; }
      50% { transform: scale(1.2); opacity: 1; }
      100% { transform: scale(0.8); opacity: 0.8; }
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>🤖 Salsabeel — Future AI Founder</h2>
    <div class="robot">
      <svg viewBox="0 0 200 260" xmlns="http://www.w3.org/2000/svg">
        <ellipse cx="100" cy="250" rx="50" ry="8" fill="rgba(0,0,0,0.4)" />
        <rect x="40" y="90" width="120" height="110" rx="20" fill="#101826" stroke="rgba(255,255,255,0.05)" />
        <rect x="80" y="60" width="40" height="30" rx="10" fill="#0b1528" />
        <rect x="60" y="20" width="80" height="50" rx="15" fill="#0c1934" stroke="rgba(255,255,255,0.05)" />
        <circle class="antenna" cx="100" cy="10" r="6" fill="url(#grad2)" />
        <circle cx="80" cy="45" r="8" fill="#6c5ce7" />
        <circle cx="120" cy="45" r="8" fill="#00d4ff" />
        <rect x="90" y="70" width="20" height="5" rx="2.5" fill="#07c3f2" />
        <defs>
          <linearGradient id="grad2" x1="0" x2="1">
            <stop offset="0%" stop-color="#6c5ce7" />
            <stop offset="100%" stop-color="#00d4ff" />
          </linearGradient>
        </defs>
      </svg>
    </div>
    <p>💻 Python • Machine Learning • Artificial Intelligence</p>
  </div>
</body>
</html>

