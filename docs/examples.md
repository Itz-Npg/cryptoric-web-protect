# Examples

Here is how you can implement Cryptoric Web Protect across various popular frameworks.

### Vanilla JavaScript
```javascript
import CryptoricProtect from "cryptoric-web-protect";

document.addEventListener("DOMContentLoaded", () => {
    CryptoricProtect.init();
    console.log("App loaded and protected!");
});
```

### React
In your `main.jsx` or `index.js`:
```jsx
import React from "react"
import ReactDOM from "react-dom/client"
import App from "./App.jsx"
import CryptoricProtect from "cryptoric-web-protect";

// Initialize immediately
CryptoricProtect.init();

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

### Next.js (App Router)
Since Next.js renders on the server, you must ensure the script only runs on the client by putting it inside a `useEffect` hook in a Client Component.

```tsx
"use client"
import { useEffect } from "react";
import CryptoricProtect from "cryptoric-web-protect";

export default function RootLayout({ children }) {
  useEffect(() => {
    CryptoricProtect.init();
  }, []);

  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```
