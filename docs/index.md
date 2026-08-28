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
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path fill-rule="evenodd" d="M12 1.5a5.25 5.25 0 0 0-5.25 5.25v3a3 3 0 0 0-3 3v6.75a3 3 0 0 0 3 3h10.5a3 3 0 0 0 3-3v-6.75a3 3 0 0 0-3-3v-3c0-2.9-2.35-5.25-5.25-5.25Zm3.75 8.25v-3a3.75 3.75 0 1 0-7.5 0v3h7.5Z" clip-rule="evenodd" /></svg>'
    details: Fades and blurs your entire website to 0% opacity instantly if the JavaScript thread is frozen by a debugger.
  - title: Instant Wipe on Shortcuts
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path fill-rule="evenodd" d="M14.615 1.595a.75.75 0 0 1 .359.852L12.982 9.75h7.268a.75.75 0 0 1 .548 1.262l-10.5 11.25a.75.75 0 0 1-1.272-.71l1.992-7.302H3.75a.75.75 0 0 1-.548-1.262l10.5-11.25a.75.75 0 0 1 .913-.143Z" clip-rule="evenodd" /></svg>'
    details: Blocks F12, Ctrl+Shift+I, and Right-Click. Any attempt to use them instantly deletes the entire DOM.
  - title: Time-Delta Wipes
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path fill-rule="evenodd" d="M12 2.25c-5.385 0-9.75 4.365-9.75 9.75s4.365 9.75 9.75 9.75 9.75-4.365 9.75-9.75S17.385 2.25 12 2.25ZM12.75 6a.75.75 0 0 0-1.5 0v6c0 .414.336.75.75.75h4.5a.75.75 0 0 0 0-1.5h-3.75V6Z" clip-rule="evenodd" /></svg>'
    details: Measures execution delays down to the millisecond to catch anyone trying to resume a paused debugger.
---
<style>
/* Add colored backgrounds to the VitePress feature icons */
.VPFeatures .item:nth-child(1) .icon { background-color: #10b981 !important; display: flex !important; justify-content: center !important; align-items: center !important; }
.VPFeatures .item:nth-child(2) .icon { background-color: #f59e0b !important; display: flex !important; justify-content: center !important; align-items: center !important; }
.VPFeatures .item:nth-child(3) .icon { background-color: #8b5cf6 !important; display: flex !important; justify-content: center !important; align-items: center !important; }
/* Ensure the SVGs are the correct size and color */
.VPFeatures .icon svg { width: 24px !important; height: 24px !important; fill: #ffffff !important; }
</style>
