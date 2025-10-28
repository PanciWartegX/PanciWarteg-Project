# PanciWarteg-Project

**Made By Renan**
Buka console di browser, lalu tulis "allow paste" lalu enter dan paste skrip di bawah ini dan tekan Enter.
tutup console agar script jalan dengan baik
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
```

> ⚠️ Hanya gunakan untuk tujuan pengujian atau pengembangan. Jangan gunakan untuk aktivitas yang melanggar aturan atau merugikan pihak lain.

---

## Cara Penggunaan

*
* 1. Buka Console
* 2.tulis "allow paste"
* 3.paste script diatas
* 4.tutup console **WAJIB!**

Catatan:

* **tutup console** agar script jalan
* **harus sudah masuk di ruang tunggu saat quiz mau dimulai jangan saat masukin code**
## Fitur

* **Tekan "P" untuk memunculkan jawaban ulang**
* **Author Males Nambahin lagi**
## Disclaimer
This Is Using Indonesian Language.

Translate It For More Information Bcz The Author Is Lazy

Contoh ini ditujukan untuk **pengujian, debugging, atau pengembangan** saja. Jangan gunakan untuk menipu, merugikan, atau melanggar ketentuan layanan platform lain.
