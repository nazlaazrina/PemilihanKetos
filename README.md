# OSISVote — Static GitHub Pages Edition

Aplikasi e-voting ketua OSIS yang **100% static**: HTML + CSS + JavaScript + `data.json`. Tidak memakai Node.js, server, database, atau folder `public`.

## Struktur
- `index.html` — halaman siswa
- `admin.html` — dashboard admin
- `css/style.css` — UI/animasi responsif
- `js/app.js` — voting/token
- `js/admin.js` — dashboard admin
- `js/crypto.js` — SHA-256 Web Crypto API
- `data.json` — data awal

## GitHub Pages
Upload seluruh isi folder ini ke repository GitHub, lalu aktifkan GitHub Pages dari branch utama. Karena ini static, `fetch('data.json')` berjalan pada GitHub Pages.

## Admin demo
PIN awal: `OSIS@2026!`

## Penting tentang keamanan
Static GitHub Pages **tidak dapat membuat admin benar-benar aman dari pengguna yang bisa membuka source code**. PIN SHA-256 hanya mencegah PIN plaintext disimpan, bukan menggantikan autentikasi server-side. Token juga hanya bisa diverifikasi di browser. Untuk tugas/demo lokal, pola ini sesuai batasan "tanpa server/database".

## "Real-time"
Perubahan antar-tab browser pada perangkat yang sama disinkronkan memakai `storage` event. GitHub Pages tidak menyediakan shared realtime state antar perangkat tanpa backend.
