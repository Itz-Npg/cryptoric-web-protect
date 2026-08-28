# Quick Start

The entire logic is heavily obfuscated and safely bundled inside the package. To secure your application, simply import and initialize it in your main entry file.

### Step 1: Import the Module
In your index.js, main.jsx, or root pp.js file:
`javascript
import CryptoricProtect from "cryptoric-web-protect";
`

### Step 2: Initialize
Call the init() method as early as possible in your application lifecycle:
`javascript
CryptoricProtect.init();
`

That's it! As soon as init() is called, the protection layer is active. 

::: warning
**Browser Environment Only:** This library relies heavily on the window and document objects. It must only run on the client-side.
:::

---

## 🛡️ Best Practices for Maximum Security

**The Golden Rule of Frontend Security:** If an attacker intercepts your website's HTML *before* it runs (using a proxy or DevTools network interception), they can simply delete the \&lt;script&gt;\ tag that loads Cryptoric Web Protect.

To prevent this and make your application truly secure, **you must intertwine the protection with your core application logic.**

### ❌ Weak Implementation
Simply calling \init()\ and moving on. If the script is deleted, the app still works perfectly.
`javascript
CryptoricProtect.init();
renderApp(); // The app loads even if protection is deleted!
`

### ✅ Strong Implementation
Make your application *rely* on the protection. If an attacker deletes the protection script, the application should crash or refuse to load your sensitive data.
`javascript
// The protection script returns true when successfully initialized
const isProtected = CryptoricProtect.init();

if (!isProtected) {
    // If the attacker deleted the script, this will trigger and crash the app
    throw new Error("Fatal: Security module missing or tampered with.");
}

// Only decrypt data or render the app if protection is actively running
decryptAPIKeys();
renderApp();
`

By tightly coupling the protection to your app's core logic, you ensure that bypassing the security completely breaks the website!
