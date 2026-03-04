<div align="center">

<h2>🛠️ Skill Radar 技能雷达图</h2>

<svg width="420" height="480" viewBox="0 0 420 480" xmlns="http://www.w3.org/2000/svg">
  <foreignObject width="420" height="480">
    <div xmlns="http://www.w3.org/1999/xhtml" style="font-family: system-ui, sans-serif; color: inherit;">

      <style>
        :root {
          --bg: #0d1117;
          --text: #c9d1d9;
          --line: #30363d;
          --fill: #58a6ff;
          --fill-opacity: 0.35;
        }
        @media (prefers-color-scheme: light) {
          :root {
            --bg: #ffffff;
            --text: #24292e;
            --line: #d0d7de;
            --fill: #0969da;
            --fill-opacity: 0.4;
          }
        }

        .radar-container {
          position: relative;
          width: 380px;
          height: 380px;
          margin: 30px auto;
          font-size: 14px;
          color: var(--text);
        }

        .radar {
          position: absolute;
          inset: 0;
          background: radial-gradient(circle at 50% 50%, transparent 30%, var(--line) 31%, transparent 32%);
          clip-path: polygon(50% 0%, 93% 34%, 81% 93%, 19% 93%, 7% 34%);
          animation: rotate 30s linear infinite;
          opacity: 0.15;
        }

        @keyframes rotate {
          to { transform: rotate(360deg); }
        }

        .radar-bg {
          position: absolute;
          inset: 0;
          background: conic-gradient(from 90deg at 50% 50%,
            transparent 0deg 72deg,
            var(--line) 72deg 73deg,
            transparent 73deg 144deg,
            var(--line) 144deg 145deg,
            transparent 145deg 216deg,
            var(--line) 216deg 217deg,
            transparent 217deg 288deg,
            var(--line) 288deg 289deg,
            transparent 289deg 360deg
          );
          clip-path: polygon(50% 0%, 93% 34%, 81% 93%, 19% 93%, 7% 34%);
          opacity: 0.6;
        }

        .radar-fill {
          position: absolute;
          inset: 0;
          background: var(--fill);
          opacity: var(--fill-opacity);
          clip-path: polygon(50% 50%, 50% 50%, 50% 50%, 50% 50%, 50% 50%);
          animation: fill-grow 3.5s ease-out forwards;
        }

        @keyframes fill-grow {
          to {
            clip-path: polygon(
              50% 50%,
              50% 0%,          /* JavaScript / 前端 */
              93% 34%,         /* Python */
              81% 93%,         /* Go / 后端 */
              19% 93%,         /* Rust / 系统 */
              7% 34%           /* TypeScript / 类型安全 */
            );
          }
        }

        .label {
          position: absolute;
          font-weight: bold;
          text-shadow: 0 0 6px rgba(0,0,0,0.6);
          pointer-events: none;
        }

        .label-1 { top: -10px;    left: 50%; transform: translateX(-50%); }
        .label-2 { top: 35%;      right: -20px; }
        .label-3 { bottom: 10%;   right: 20%; }
        .label-4 { bottom: 10%;   left: 20%; }
        .label-5 { top: 35%;      left: -20px; }

        .value {
          font-size: 0.9em;
          opacity: 0.8;
          margin-top: 4px;
        }
      </style>

      <div class="radar-container">

        <div class="radar-bg"></div>
        <div class="radar"></div>

        <!-- 核心技能填充区域（改这里的 clip-path 数值来调整形状） -->
        <div class="radar-fill" style="animation-delay: 0.4s;"></div>

        <!-- 五个标签 + 熟练度（0-100） -->
        <div class="label label-1">
          JavaScript<br><span class="value">95</span>
        </div>
        <div class="label label-2">
          Python<br><span class="value">88</span>
        </div>
        <div class="label label-3">
          Go<br><span class="value">82</span>
        </div>
        <div class="label label-4">
          Rust<br><span class="value">75</span>
        </div>
        <div class="label label-5">
          TypeScript<br><span class="value">92</span>
        </div>

      </div>

    </div>
  </foreignObject>
</svg>

<p><small>鼠标悬停在 GitHub 页面有时会看到更明显的动画效果～</small></p>

</div>
