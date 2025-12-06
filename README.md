<!-- HEADER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=160&text=Nyxaroth&fontAlign=50&fontAlignY=40&color=a26bfa&fontColor=ffffff&section=header" />
</p>

> minimal purple noir profile  
> visuals live on the portfolio, logic lives here

```text
nyx@core:~$ cat profile.txt
```
theme:          purple noir
mode:           quiet but intentional
location:       github profile

> whoami

creative developer who likes clean systems, small tools and good aesthetics
treats code as something that should feel nice to read and work with

> projects

1. Nyx VS Code Theme
   - purple focused editor theme
   - tuned for long sessions and clear contrast

2. signal_studio
   - playground for signals and reactive ideas
   - experiments in TypeScript and UI logic

3. BGMI Roster Bot (private)
   - tracks roster moves and posts to X
   - live feed: @BgmiUpdateBot

> portfolio

url:  https://nyxaroth.vercel.app
note: full visual identity and case studies live there

> status

- refining minimal noir design language
- turning experiments into reusable components
- iterating on signal_studio interactions

> contact

email: nyxaroth.vt@gmail.com
bgmi:  https://x.com/BgmiUpdateBot

> exit

session closed

class NyxSystem {
  constructor(
    private mode: "silent" | "focused" = "focused",
    private theme: "purple_noir" | "plain" = "purple_noir"
  ) {}

  boot() {
    return {
      status: "online",
      mode: this.mode,
      theme: this.theme,
      timestamp: new Date().toISOString()
    };
  }
}

const nyx = new NyxSystem("focused", "purple_noir");
nyx.boot();
