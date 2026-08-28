---
layout: home
hero:
  name: "Cryptoric Web Protect"
  text: "Military-Grade Anti-DevTools & Web Protection Library."
  tagline: "Aggressively prevent reverse engineering, code inspection, and tampering of your web applications with zero configuration."
  actions:
    - theme: brand
      text: Get Started
      link: /introduction
    - theme: alt
      text: View on GitHub
      link: https://github.com/Itz-Npg/cryptoric-web-protect
features:
  - title: Dual-Class CSS Dead-Man's Switch
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="9" cy="12" r="1"/><circle cx="15" cy="12" r="1"/><path d="M8 20v2h8v-2"/><path d="m12.5 17-.5-1-.5 1h1z"/><path d="M16 20a2 2 0 0 0 1.56-3.25 8 8 0 1 0-11.12 0A2 2 0 0 0 8 20"/></svg>'
    details: Fades and blurs your entire website to 0% opacity instantly if the JavaScript thread is frozen by a debugger.
  - title: Instant Wipe on Shortcuts
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M10 8h.01"/><path d="M12 12h.01"/><path d="M14 8h.01"/><path d="M16 12h.01"/><path d="M18 8h.01"/><path d="M6 8h.01"/><path d="M7 16h10"/><path d="M8 12h.01"/><rect width="20" height="16" x="2" y="4" rx="2"/></svg>'
    details: Blocks F12, Ctrl+Shift+I, and Right-Click. Any attempt to use them instantly deletes the entire DOM.
  - title: Time-Delta Wipes
    icon: '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="10" x2="14" y1="2" y2="2"/><line x1="12" x2="15" y1="14" y2="11"/><circle cx="12" cy="14" r="8"/></svg>'
    details: Measures execution delays down to the millisecond to catch anyone trying to resume a paused debugger.
---
<style>
/* Add colored backgrounds to the VitePress feature icons */
.VPFeatures .item:nth-child(1) .icon { background-color: #ef4444 !important; }
.VPFeatures .item:nth-child(2) .icon { background-color: #3b82f6 !important; }
.VPFeatures .item:nth-child(3) .icon { background-color: #f59e0b !important; }
/* Ensure the icons inside remain white */
.VPFeatures .icon svg { stroke: #ffffff !important; color: #ffffff !important; }
</style>
