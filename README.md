## Load via raw.githubusercontent.com (provided URL)

File:
`https://raw.githubusercontent.com/PanciWartegX/PanciWarteg-Project/refs/heads/main/main%20script.js`

> NOTE: raw.githubusercontent.com seringkali dapat di-fetch sebagai teks, tetapi **tidak selalu** optimal untuk `import()` sebagai ES module karena header MIME / CORS. Jika import dynamic gagal, gunakan metode fetch + inject (Blob).

### Dynamic import (tidak direkomendasikan untuk raw.githubusercontent.com)
```javascript
// Mungkin gagal karena CORS/MIME
const rawUrl = 'https://raw.githubusercontent.com/PanciWartegX/PanciWarteg-Project/refs/heads/main/main%20script.js';

import(rawUrl)
  .then(mod => console.log('Module loaded', mod))
  .catch(err => console.error('Import gagal (raw):', err));
