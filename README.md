# catmuseum form — 100% statis

Cuma 1 file: `index.html`. Tidak ada server, bot, worker, atau backend apa pun.

## Cara kerja

Form ini **tidak meminta upload foto atau lagu sama sekali** — buyer cukup isi data teksnya. Untuk foto & lagu, mereka kirim langsung di chat Telegram (sekali saja, di sana), jadi tidak ada acara pilih-file-dua-kali.

Alurnya:
1. Buyer isi semua kolom teks (kalau ada yang kosong, tombol **submit** tidak akan lanjut).
2. Tekan **submit** → teks ringkasan pesanan otomatis tersalin ke clipboard, dan tab **t.me/mirssy** otomatis terbuka dengan teks itu **sudah terisi** di kolom chat (buyer tidak perlu ketik/paste apa pun — Telegram mendukung link dengan pesan pra-isi).
3. Buyer tinggal tap **kirim**, lalu langsung attach **6 foto memory wall** dan **1 file lagu .mp3** di chat yang sama.

## Hosting di GitHub Pages

1. [github.com](https://github.com) → login → **+ → New repository** → nama bebas → **Public** → **Create repository**.
2. **uploading an existing file** → upload `index.html` → **Commit changes**.
3. **Settings → Pages → Source**: `Deploy from a branch`, branch `main`, folder `/ (root)` → **Save**.
4. Tunggu ±1 menit → link situs muncul: `https://NAMAKAMU.github.io/nama-repo/`

Itu link yang dikasih ke customer. Nama file **harus** `index.html`.

## Update form nanti

Buka file di repo → ikon pensil (**Edit**) → paste versi baru → **Commit changes**. GitHub Pages update otomatis ±1 menit.

## Ganti username Telegram tujuan

Cari baris ini di `index.html`:
```js
const TELEGRAM_USERNAME = 'mirssy';
```
Ganti sesuai kebutuhan, lalu commit ulang.
