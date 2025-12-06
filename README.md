<!-- HEADER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=160&text=Nyxaroth&fontAlign=50&fontAlignY=40&color=a26bfa&fontColor=ffffff&section=header" />
</p>

<style>
  .nyx-terminal-wrapper {
    font-family: "Fira Code", Menlo, Monaco, Consolas, monospace;
    display: flex;
    justify-content: center;
    margin: 0 auto 24px auto;
    padding: 0 12px;
  }

  .nyx-terminal-inner {
    max-width: 720px;
    width: 100%;
  }

  .nyx-theme-select {
    text-align: right;
    margin-bottom: 6px;
  }

  .nyx-theme-select input {
    display: none;
  }

  .nyx-theme-select label {
    display: inline-block;
    padding: 4px 10px;
    margin-left: 4px;
    font-size: 11px;
    cursor: pointer;
    border-radius: 999px;
    border: 1px solid #2d2d3a;
    background: #06040c;
    color: #d7d7f0;
    user-select: none;
    transition: background 0.2s ease, color 0.2s ease, border-color 0.2s ease, transform 0.1s ease;
  }

  .nyx-theme-select label:hover {
    transform: translateY(-1px);
  }

  #nyx-theme-purple:checked + label {
    background: #a26bfa;
    color: #05010a;
    border-color: #c4a5ff;
  }

  #nyx-theme-cyan:checked + label {
    background: #22d3ee;
    color: #020617;
    border-color: #6be7fb;
  }

  #nyx-theme-amber:checked + label {
    background: #fbbf24;
    color: #111827;
    border-color: #fde68a;
  }

  .nyx-terminal {
    --nyx-bg: #05010a;
    --nyx-border: #a26bfa;
    --nyx-header-bg: #090315;
    --nyx-header-text: #e5e5ff;
    --nyx-text-main: #e5e5ff;
    --nyx-text-soft: #9ca3af;
    --nyx-accent: #a26bfa;
    --nyx-prompt: #a855f7;
    --nyx-command: #fbbf24;
    --nyx-link: #c4b5fd;

    background: radial-gradient(circle at top left, #10041f 0, #020010 45%, #02010a 100%);
    border-radius: 14px;
    border: 1px solid var(--nyx-border);
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.65);
    overflow: hidden;
  }

  #nyx-theme-purple:checked ~ .nyx-terminal {
    --nyx-bg: #05010a;
    --nyx-border: #a26bfa;
    --nyx-header-bg: #0b0319;
    --nyx-header-text: #f5f3ff;
    --nyx-text-main: #e5e7ff;
    --nyx-text-soft: #9ca3af;
    --nyx-accent: #a26bfa;
    --nyx-prompt: #a855f7;
    --nyx-command: #fbbf24;
    --nyx-link: #c4b5fd;
  }

  #nyx-theme-cyan:checked ~ .nyx-terminal {
    --nyx-bg: #01101a;
    --nyx-border: #22d3ee;
    --nyx-header-bg: #021520;
    --nyx-header-text: #e0faff;
    --nyx-text-main: #e0f2fe;
    --nyx-text-soft: #9ca3b0;
    --nyx-accent: #22d3ee;
    --nyx-prompt: #22c1ee;
    --nyx-command: #a5b4fc;
    --nyx-link: #7dd3fc;
  }

  #nyx-theme-amber:checked ~ .nyx-terminal {
    --nyx-bg: #1a1001;
    --nyx-border: #fbbf24;
    --nyx-header-bg: #171002;
    --nyx-header-text: #fef9c3;
    --nyx-text-main: #fef3c7;
    --nyx-text-soft: #a3a39a;
    --nyx-accent: #fbbf24;
    --nyx-prompt: #f59e0b;
    --nyx-command: #bfdbfe;
    --nyx-link: #fed7aa;
  }

  .nyx-terminal-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: linear-gradient(90deg, var(--nyx-header-bg), #02010a);
    padding: 6px 10px;
    border-bottom: 1px solid rgba(148, 163, 184, 0.25);
  }

  .nyx-dots {
    display: flex;
    gap: 5px;
  }

  .nyx-dot {
    width: 9px;
    height: 9px;
    border-radius: 999px;
    background: #4b5563;
  }

  .nyx-dot:nth-child(1) {
    background: #f97373;
  }

  .nyx-dot:nth-child(2) {
    background: #facc15;
  }

  .nyx-dot:nth-child(3) {
    background: #4ade80;
  }

  .nyx-title {
    font-size: 11px;
    color: var(--nyx-header-text);
    letter-spacing: 0.06em;
    text-transform: uppercase;
    opacity: 0.85;
  }

  .nyx-terminal-body {
    background: radial-gradient(circle at top left, rgba(162, 107, 250, 0.1), transparent 55%), var(--nyx-bg);
    padding: 12px 14px 14px 14px;
    color: var(--nyx-text-main);
    font-size: 12px;
    line-height: 1.5;
  }

  .nyx-line {
    white-space: pre-wrap;
    word-break: break-word;
  }

  .nyx-line + .nyx-line {
    margin-top: 2px;
  }

  .nyx-prompt {
    color: var(--nyx-prompt);
  }

  .nyx-command {
    color: var(--nyx-command);
  }

  .nyx-soft {
    color: var(--nyx-text-soft);
  }

  .nyx-accent {
    color: var(--nyx-accent);
  }

  .nyx-link {
    color: var(--nyx-link);
    text-decoration: none;
  }

  .nyx-link:hover {
    text-decoration: underline;
  }

  .nyx-section-spacer {
    margin-top: 7px;
  }

  .nyx-blink {
    display: inline-block;
    width: 7px;
    height: 12px;
    margin-left: 3px;
    background: var(--nyx-accent);
    animation: nyx-caret 1.1s step-end infinite;
  }

  @keyframes nyx-caret {
    0%, 60% {
      opacity: 1;
    }
    60.01%, 100% {
      opacity: 0;
    }
  }

  .nyx-footer {
    text-align: center;
    font-family: "Fira Code", Menlo, Monaco, Consolas, monospace;
    font-size: 11px;
    color: #6b7280;
    margin: 8px 0 0 0;
  }

  .nyx-footer span {
    color: #a26bfa;
  }
</style>

<div class="nyx-terminal-wrapper">
  <div class="nyx-terminal-inner">

    <div class="nyx-theme-select">
      <span style="font-size:11px;color:#6b7280;margin-right:4px;">theme</span>
      <input type="radio" name="nyx-theme" id="nyx-theme-purple" checked>
      <label for="nyx-theme-purple">purple</label>
      <input type="radio" name="nyx-theme" id="nyx-theme-cyan">
      <label for="nyx-theme-cyan">cyan</label>
      <input type="radio" name="nyx-theme" id="nyx-theme-amber">
      <label for="nyx-theme-amber">amber</label>
    </div>

    <div class="nyx-terminal">
      <div class="nyx-terminal-header">
        <div class="nyx-dots">
          <span class="nyx-dot"></span>
          <span class="nyx-dot"></span>
          <span class="nyx-dot"></span>
        </div>
        <div class="nyx-title">nyxaroth • interactive shell</div>
        <div style="width:40px;"></div>
      </div>
      <div class="nyx-terminal-body">
        <div class="nyx-line nyx-soft">system boot complete. navigating profile through shell.</div>
        <div class="nyx-line nyx-soft">type like a dev, browse like a visitor.</div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">whoami</span>
        </div>
        <div class="nyx-line">
          minimal dev with a focus on aesthetics, small tools and clean systems.
        </div>
        <div class="nyx-line">
          mixing design sense with late night experiments and intentional builds.
        </div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">projects</span>
        </div>
        <div class="nyx-line nyx-soft">listing tracked work items...</div>
        <div class="nyx-line">- Nyx VS Code Theme</div>
        <div class="nyx-line">- signal_studio</div>
        <div class="nyx-line">- BGMI Roster Bot (private)</div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">open portfolio</span>
        </div>
        <div class="nyx-line">
          visual profile at <a class="nyx-link" href="https://nyxaroth.vercel.app/">https://nyxaroth.vercel.app/</a>
        </div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">status</span>
        </div>
        <div class="nyx-line">- building tools that feel intentional instead of loud</div>
        <div class="nyx-line">- refining small experiments into reusable pieces</div>
        <div class="nyx-line">- keeping github focused while portfolio holds the visuals</div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">contact</span>
        </div>
        <div class="nyx-line">
          email  - <a class="nyx-link" href="mailto:nyxaroth.vt@gmail.com">nyxaroth.vt@gmail.com</a>
        </div>
        <div class="nyx-line">
          bgmi   - <a class="nyx-link" href="https://x.com/BgmiUpdateBot">https://x.com/BgmiUpdateBot</a>
        </div>

        <div class="nyx-section-spacer"></div>

        <div class="nyx-line">
          <span class="nyx-prompt">nyx@core</span>:<span class="nyx-soft">~</span>$ <span class="nyx-command">exit</span>
          <span class="nyx-blink"></span>
        </div>
      </div>
    </div>

    <p class="nyx-footer">
      <span>&gt;</span> running in minimal purple noir mode
    </p>

  </div>
</div>
