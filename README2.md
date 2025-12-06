<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>nyxaroth • terminal</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #05010a;
      --border: #a26bfa;
      --header-bg: #0b0319;
      --text-main: #e5e7ff;
      --text-soft: #9ca3af;
      --accent: #a26bfa;
      --prompt: #a855f7;
      --command: #fbbf24;
      --link: #c4b5fd;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, #111827, #02010a);
      font-family: "Fira Code", monospace;
      color: var(--text-main);
    }

    .shell-wrap {
      max-width: 760px;
      width: 100%;
      padding: 20px;
      box-sizing: border-box;
    }

    .theme-switcher {
      text-align: right;
      font-size: 11px;
      color: #9ca3af;
      margin-bottom: 6px;
    }

    .theme-switcher button {
      border-radius: 999px;
      border: 1px solid #4c1d95;
      background: #020010;
      color: var(--text-main);
      font-family: inherit;
      font-size: 11px;
      padding: 4px 10px;
      margin-left: 4px;
      cursor: pointer;
      transition: background 0.15s ease, color 0.15s ease, border-color 0.15s ease, transform 0.08s ease;
    }

    .theme-switcher button:hover {
      transform: translateY(-1px);
    }

    .theme-switcher button.active {
      background: var(--accent);
      color: #020617;
      border-color: #e5e7ff;
    }

    .terminal {
      background: radial-gradient(circle at top left, rgba(162, 107, 250, 0.16), transparent 55%), var(--bg);
      border-radius: 14px;
      border: 1px solid var(--border);
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.65);
      overflow: hidden;
    }

    .terminal-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 6px 10px;
      background: linear-gradient(90deg, var(--header-bg), #020008);
      border-bottom: 1px solid rgba(148, 163, 184, 0.3);
      font-size: 11px;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: #f5f3ff;
    }

    .dots {
      display: flex;
      gap: 5px;
    }

    .dot {
      width: 9px;
      height: 9px;
      border-radius: 999px;
    }
    .dot.red { background: #f97373; }
    .dot.yellow { background: #facc15; }
    .dot.green { background: #4ade80; }

    .terminal-body {
      padding: 12px 14px 14px 14px;
      font-size: 12px;
      line-height: 1.5;
    }

    .line { white-space: pre-wrap; word-break: break-word; }
    .line + .line { margin-top: 2px; }

    .soft { color: var(--text-soft); }
    .prompt { color: var(--prompt); }
    .command { color: var(--command); }
    .link { color: var(--link); text-decoration: none; }
    .link:hover { text-decoration: underline; }

    .spacer { height: 7px; }

    .caret {
      display: inline-block;
      width: 7px;
      height: 12px;
      margin-left: 3px;
      background: var(--accent);
      animation: caret 1.1s step-end infinite;
    }

    @keyframes caret {
      0%, 60% { opacity: 1; }
      60.01%, 100% { opacity: 0; }
    }

    .footer {
      margin-top: 8px;
      text-align: center;
      font-size: 11px;
      color: #9ca3af;
    }

    .footer span {
      color: var(--accent);
    }
  </style>
</head>
<body>
  <div class="shell-wrap">
    <div class="theme-switcher">
      theme:
      <button data-theme="purple" class="active">purple</button>
      <button data-theme="cyan">cyan</button>
      <button data-theme="amber">amber</button>
    </div>

    <div class="terminal">
      <div class="terminal-header">
        <div class="dots">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
        </div>
        <div>nyxaroth · interactive shell</div>
        <div style="width:40px;"></div>
      </div>
      <div class="terminal-body">
        <div class="line soft">system boot complete. navigating profile through shell.</div>
        <div class="line soft">press theme buttons to rotate color context.</div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> whoami</span>
        </div>
        <div class="line">minimal dev with a bias for aesthetics, small tools and clean systems.</div>
        <div class="line">builds things that feel intentional, not noisy.</div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> projects</span>
        </div>
        <div class="line soft">listing tracked work items...</div>
        <div class="line">- Nyx VS Code Theme</div>
        <div class="line">- signal_studio</div>
        <div class="line">- BGMI Roster Bot (private)</div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> open portfolio</span>
        </div>
        <div class="line">
          visual profile at <a href="https://nyxaroth.vercel.app/" class="link">https://nyxaroth.vercel.app/</a>
        </div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> status</span>
        </div>
        <div class="line">- refining small experiments into reusable systems</div>
        <div class="line">- keeping github focused while portfolio carries visuals</div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> contact</span>
        </div>
        <div class="line">
          email  - <a href="mailto:nyxaroth.vt@gmail.com" class="link">nyxaroth.vt@gmail.com</a>
        </div>
        <div class="line">
          bgmi   - <a href="https://x.com/BgmiUpdateBot" class="link">https://x.com/BgmiUpdateBot</a>
        </div>

        <div class="spacer"></div>

        <div class="line">
          <span class="prompt">nyx@core</span>:<span class="soft">~$</span><span class="command"> exit</span><span class="caret"></span>
        </div>
      </div>
    </div>

    <div class="footer">
      &gt; running in <span>minimal purple noir</span> environment
    </div>
  </div>

  <script>
    const purple = {
      bg: "#05010a",
      border: "#a26bfa",
      headerBg: "#0b0319",
      textMain: "#e5e7ff",
      textSoft: "#9ca3af",
      accent: "#a26bfa",
      prompt: "#a855f7",
      command: "#fbbf24",
      link: "#c4b5fd"
    };

    const cyan = {
      bg: "#01101a",
      border: "#22d3ee",
      headerBg: "#031623",
      textMain: "#e0f2fe",
      textSoft: "#9ca3b0",
      accent: "#22d3ee",
      prompt: "#06b6d4",
      command: "#a5b4fc",
      link: "#7dd3fc"
    };

    const amber = {
      bg: "#1a1001",
      border: "#fbbf24",
      headerBg: "#171002",
      textMain: "#fef3c7",
      textSoft: "#a3a39a",
      accent: "#fbbf24",
      prompt: "#f59e0b",
      command: "#bfdbfe",
      link: "#fed7aa"
    };

    const themes = { purple, cyan, amber };

    const buttons = document.querySelectorAll("[data-theme]");

    function applyTheme(name) {
      const t = themes[name] || purple;
      document.documentElement.style.setProperty("--bg", t.bg);
      document.documentElement.style.setProperty("--border", t.border);
      document.documentElement.style.setProperty("--header-bg", t.headerBg);
      document.documentElement.style.setProperty("--text-main", t.textMain);
      document.documentElement.style.setProperty("--text-soft", t.textSoft);
      document.documentElement.style.setProperty("--accent", t.accent);
      document.documentElement.style.setProperty("--prompt", t.prompt);
      document.documentElement.style.setProperty("--command", t.command);
      document.documentElement.style.setProperty("--link", t.link);

      buttons.forEach(btn => {
        btn.classList.toggle("active", btn.dataset.theme === name);
      });
    }

    buttons.forEach(btn => {
      btn.addEventListener("click", () => applyTheme(btn.dataset.theme));
    });

    applyTheme("purple");
  </script>
</body>
</html>
