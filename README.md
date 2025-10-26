## Load via raw.githubusercontent.com (provided URL)

File:
`https://raw.githubusercontent.com/PanciWartegX/PanciWarteg-Project/refs/heads/main/main%20script.js`

> NOTE: raw.githubusercontent.com seringkali dapat di-fetch sebagai teks, tetapi **tidak selalu** optimal untuk `import()` sebagai ES module karena header MIME / CORS. Jika import dynamic gagal, gunakan metode fetch + inject (Blob).

### Dynamic import (tidak direkomendasikan untuk raw.githubusercontent.com)
```javascript
(async () => {
  const rawUrl = 'https://raw.githubusercontent.com/PanciWartegX/PanciWarteg-Project/refs/heads/main/main%20script.js';
  try {
    const res = await fetch(rawUrl);
    if (!res.ok) throw new Error(`HTTP ${res.status}`);
    const jsText = await res.text();
    const blob = new Blob([jsText], { type: 'application/javascript' });
    const blobUrl = URL.createObjectURL(blob);
    const s = document.createElement('script');
    s.src = blobUrl;
    document.head.appendChild(s);
    s.onload = () => {
      URL.revokeObjectURL(blobUrl);
      console.log('Script dimuat dari Blob (raw URL)');
    };
  } catch (e) {
    console.error('Gagal memuat script dari raw URL:', e);
  }
})();
