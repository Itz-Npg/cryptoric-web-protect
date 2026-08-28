# Quick Start

The entire logic is heavily obfuscated and safely bundled inside the package. To secure your application, simply import and initialize it in your main entry file.

### Step 1: Import the Module
In your `index.js`, `main.jsx`, or root `app.js` file:
```javascript
import CryptoricProtect from "cryptoric-web-protect";
```

### Step 2: Initialize
Call the `init()` method as early as possible in your application lifecycle:
```javascript
CryptoricProtect.init();
```

That's it! As soon as `init()` is called, the protection layer is active. 

::: warning
**Browser Environment Only:** This library relies heavily on the `window` and `document` objects. It must only run on the client-side.
:::
