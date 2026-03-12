# Dave Drummond — Device Profile
*For use in all MyMonopolyPortal / ANAND Holdings sessions*

## Primary Device
- **Type:** Android Phone (Mobile)
- **Browser:** Chrome for Android (based on URL bar style in screenshots)
- **Screen:** ~393px viewport width (standard Android flagship)
- **OS:** Android (recent — based on nav bar style)
- **Orientation:** Portrait primary

## Screenshot Handling
- Dave sends screenshots for UI debugging
- **Protocol:** Look and immediately delete (uploads are read-only on Claude's end — inform Dave)
- Compress/shrink screenshots before sending if possible to save context space

## Mobile CSS Breakpoints (confirmed working)
- Use `max-width: 650px` for mobile overrides
- Use `100svh` (small viewport height) not `100vh` — accounts for Android Chrome browser chrome
- Card height formula: `calc(100svh - 120px)` for ANAND deck on mobile
- Card width formula: `calc(100vw - 32px)` for full-bleed mobile cards

## Known Mobile Issues (fixed)
- Login input `id="pi"` conflicted with JS — renamed to `id="pwd"` ✅
- Card height `760px` exceeded phone viewport — fixed to `100svh - 120px` ✅
- Porthole lens `320px` too large on phone — reduced to `220px` on mobile ✅
- Ghost cards behind lens scaled down for mobile ✅

## GitHub Workflow
- Dave's repo: `FSIExperts/ANANDPortfolio`
- Dave pushes files manually from local machine
- Claude drops files to `/mnt/user-data/outputs/` for Dave to download
- No direct GitHub push from Claude unless GH_TOKEN provided in session

## Preferred Workflow
- Claude makes edits to project files
- Presents output file for download
- Dave takes to GitHub manually
- OR Dave provides GitHub PAT in portal for in-app saves

## Android → GitHub Tools (recommended)
See separate section in this file below.

---

## Android GitHub Tools

### Best Options for Android:

**1. GitHub Mobile App (Official)**
- Free, by GitHub
- View/edit files, manage PRs, review code
- *Cannot* upload arbitrary files or drag-drop HTML
- Best for: reviewing changes, merging PRs

**2. Working Copy** *(iOS only — not available Android)*

**3. Spck Code Editor**
- Android code editor with Git built in
- Can clone repo, edit files, commit and push
- Free tier available
- Best for: editing HTML/CSS directly on phone

**4. MGit**
- Free Git client for Android
- Clone, pull, push repos
- Pair with any text editor
- Best for: managing repo files on phone

**5. Termux + Git** *(Power user)*
- Full Linux terminal on Android
- `pkg install git` then standard git workflow
- Most powerful option — full control
- Best for: Dave if comfortable with terminal

**6. GitHub Web (Chrome Mobile)**
- Go to github.com on Chrome
- Navigate to file → Edit (pencil icon)
- Paste updated HTML → Commit
- Best for: quick single-file updates like `anand-holdings-v4.html`
- **This is probably Dave's easiest path right now**

### Recommended for Dave:
**GitHub Web via Chrome** for quick HTML file updates +  
**GitHub Mobile App** for repo management and monitoring

