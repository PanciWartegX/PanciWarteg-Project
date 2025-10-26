# PanciWarteg-Project

This repository contains an obfuscated script `obfuscated.js` and examples how to load it from a browser.

> ⚠️ Security & ethics: only use this code for legitimate testing or development. Do **not** use it to cheat or to violate terms of service.

## Load via dynamic import (recommended)

Modern browsers that support ES modules can dynamically import the script:

```javascript
// Pakai CDN jsDelivr agar CORS/MIME lebih andal
const url = 'https://cdn.jsdelivr.net/gh/PanciWartegX/PanciWarteg-Project@main/obfuscated.js';

import(url)
  .then(mod => {
    console.log('Module loaded', mod);
    // gunakan export dari module (jika ada)
  })
  .catch(err => console.error('Import gagal:', err));
