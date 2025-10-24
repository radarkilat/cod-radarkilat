# Maritoko Pages (Landing: Topi Bisbol)

Landing page statis untuk **Cloudflare Pages** (bisa juga GitHub Pages).

## Struktur
```
.
├─ index.html                # Redirect ke /topi-bisbol/
├─ _redirects                # Rules untuk Cloudflare Pages
├─ topi-bisbol/
│  └─ index.html             # Landing produk
└─ .nojekyll                 # (opsional) supaya GitHub Pages tidak menjalankan Jekyll
```

## Konfigurasi cepat
Edit variabel di `topi-bisbol/index.html` bagian **CONFIG**:
```js
const PRODUCT_ID   = 477;                           // ID WooCommerce
const CHECKOUT_URL = "https://maritoko.com/checkout/";
const WA_NUMBER    = "6285178200718";               // tanpa +
const WA_TEXT      = "Halo admin Maritoko, saya mau Topi Bisbol Unisex. Apakah ready?";
```

## Deploy ke Cloudflare Pages
1. Buat repo GitHub, push semua file ini (lihat langkah Git di bawah).
2. Cloudflare Pages → Create a project → Connect to Git → pilih repo ini.
3. Build settings: **Framework preset = None**, **Build command = (kosong)**, **Output directory = /**
4. (Opsional) Custom domain → tambahkan `produk-digital.maritoko.com`.

## Deploy ke GitHub Pages (opsional)
- Settings → Pages → Source: **GitHub Actions** atau **Deploy from a branch** (main / root).
- Jika pakai GitHub Pages, file `_redirects` diabaikan—redirect sudah di-handle oleh `index.html` dengan meta refresh + JS.

## Langkah Git (copy–paste)
```bash
git init
git add .
git commit -m "init: maritoko pages"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```

---

*Generated on 2025-10-23T17:06:16.172215Z*
