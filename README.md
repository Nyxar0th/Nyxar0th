<!-- HEADER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=160&text=Nyxaroth&fontAlign=50&fontAlignY=40&color=a26bfa&fontColor=ffffff&section=header" />
</p>

> minimal purple noir profile  
> visuals live on the portfolio, logic lives here

```text
nyx@core:~$ cat profile.txt

theme:          purple noir
mode:           focused but quiet
location:       github profile

> whoami
creative developer who likes clean systems, small tools and intentional aesthetics
treats code as something that should feel good to read and work with

> projects
1. Nyx VS Code Theme
   - purple focused editor theme
   - tuned for long sessions and clean contrast

2. signal_studio
   - playground for signals and reactive UI ideas
   - experiments in TypeScript and component logic

3. BGMI Roster Bot (private)
   - parses roster movement data and posts updates to X
   - live feed: @BgmiUpdateBot

> portfolio
url:  https://nyxaroth.vercel.app
note: full visual identity and showcases live there

> status
- refining minimal noir design language
- turning experiments into reusable components
- iterating on signal_studio interactions

> contact
email: nyxaroth.vt@gmail.com
bgmi:  https://x.com/BgmiUpdateBot

> exit
session closed
```

```ts
// code_showcase.ts
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
      timestamp: new Date().toISOString(),
    };
  }
}

const nyx = new NyxSystem("focused", "purple_noir");
nyx.boot();
```
