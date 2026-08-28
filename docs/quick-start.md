# Quick Start

The entire logic is heavily obfuscated and safely bundled inside the package. To secure your application, you must initialize it before your main application code runs.

## Scenario 1: Modern Frameworks (React, Next.js, Vite, Vue)

If you are using a modern JavaScript framework with a bundler, NPM handles everything for you automatically.

### Step 1: Import the Module
In your `index.js`, `main.jsx`, or root `App.js` file:
```javascript
import CryptoricProtect from "cryptoric-web-protect";
```

### Step 2: Initialize
Call the `init()` method as early as possible in your application lifecycle:
```javascript
CryptoricProtect.init();
```

---

## Scenario 2: Plain HTML Sites (No Bundler)

If you are building a traditional website using plain HTML, CSS, and JS (or PHP), browsers cannot directly import from the `node_modules` folder. 

The easiest way to use the library is via our **free CDN link**, which automatically serves the NPM package over the internet. You do not need to download or copy any files!

Just paste this into the `<head>` of your HTML document:
```html
<script src="https://unpkg.com/cryptoric-web-protect@1.0.5/cryptoric-web-protect.js"></script>
<script>
    window.CryptoricProtect.init();
</script>
```

::: warning
**Browser Environment Only:** This library relies heavily on the `window` and `document` objects. It must only run on the client-side.
:::

---

## 🛡️ Best Practices for Maximum Security

**The Golden Rule of Frontend Security:** If an attacker intercepts your website's HTML *before* it runs (using a proxy or DevTools network interception), they can simply delete the `<script>` tag that loads Cryptoric Web Protect.

To prevent this and make your application truly secure, **you must intertwine the protection with your core application logic.**

### ❌ Weak Implementation
Simply calling `init()` and moving on. If the script is deleted, the app still works perfectly.
```javascript
CryptoricProtect.init();
renderApp(); // The app loads even if protection is deleted!
```

### ✅ Strong Implementation
Make your application *rely* on the protection. If an attacker deletes the protection script, the application should crash or refuse to load your sensitive data.
```javascript
// The protection script returns true when successfully initialized
const isProtected = CryptoricProtect.init();

if (!isProtected) {
    // If the attacker deleted the script, this will trigger and crash the app
    throw new Error("Fatal: Security module missing or tampered with.");
}

// Only decrypt data or render the app if protection is actively running
decryptAPIKeys();
renderApp();
```

By tightly coupling the protection to your app's core logic, you ensure that bypassing the security completely breaks the website!
