# Features

Cryptoric Web Protect deploys 5 separate layers of aggressive defense mechanisms:

### 1. Dual-Class CSS Dead-Man's Switch ☠️
If an attacker manages to force open DevTools (e.g., via the Chrome menu) and pauses your website using the debugger, our script stops running. When the JavaScript thread freezes, a pure CSS animation takes over, blurring your entire website and fading it to 0% opacity within 1 second. The attacker will just stare at a blank, unreadable screen.

### 2. Time-Delta DOM Wipe ⏱️
If an attacker tries to unpause the frozen debugger, the script measures the exact millisecond delay that occurred while it was paused. Detecting the unnatural delay, it instantly executes document.body.innerHTML = "" to delete your entire website structure.

### 3. Instant Wipe on Shortcuts ⌨️
It actively listens for and blocks the following developer shortcuts:
- F12
- Ctrl + Shift + I (Inspect)
- Ctrl + Shift + C (Element Select)
- Ctrl + U (View Source)
- Right-Click (Context Menu)

If a user even *presses* these keys, it doesn't just block them—it instantly wipes the screen blank as punishment.

### 4. Docked DevTools Detection 🪟
If an attacker tries to dock DevTools to the side or bottom of their browser, the script detects the sudden unnatural difference between the "Outer Window Size" and "Inner Window Size" and instantly wipes the page.

### 5. Nuclear Console Trap ☢️
It drops a fake "bait" object into the background console. If the DevTools Console tab is opened, the browser automatically tries to read this bait object, which triggers an instant, complete page wipe.
