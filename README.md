# Tic Tac Toe (Multiplayer) — FastAPI

Aplikasi permainan Tic Tac Toe (3x3) multiplayer sederhana dengan FastAPI. Bisa bermain berdua (teman) atau lawan komputer. Tampilan sudah bertema gelap (black theme).

## Fitur
- Buat ruangan (room) dan bagikan ID ke teman
- Gabung ke ruangan menggunakan ID
- Mode lawan komputer (AI random)
- Update game via WebSocket (localhost) atau polling (Vercel)
- Reset game kapan saja

## Persyaratan
- Python 3.10+
- Pip

## Cara Menjalankan (Lokal)
1. Buka folder proyek:
   ```bash
   cd "tic tac toe"
   ```
2. (Opsional) Buat virtual environment dan aktifkan:
   ```bash
   python -m venv .venv
   # Git Bash
   source .venv/Scripts/activate
   # PowerShell
   # .\.venv\Scripts\Activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Jalankan server:
   ```bash
   python main.py
   # atau
   # uvicorn main:app --reload --host 127.0.0.1 --port 8000
   ```
5. Buka di browser: `http://127.0.0.1:8000/`

## Cara Main
- Buat ruangan: isi Nama Ruangan, Nama Kamu, (opsional) Kata Sandi, lalu klik “Buat Ruangan”.
- Bagikan Room ID ke teman agar bisa gabung.
- Atau gunakan “Lawan Komputer”.
- Klik kotak pada papan 3x3 untuk menaruh X/O. Pemain 1 = X, Pemain 2 = O.
- Klik “Ulangi Permainan” untuk reset.

## Deploy ke Vercel
Proyek sudah menyertakan `vercel.json`. Di Vercel, WebSocket dibatasi; aplikasi otomatis memakai polling.

## Struktur Proyek (folder ini)
- `main.py` — API FastAPI (rooms, moves, game state)
- `static/index.html` — UI game (HTML, CSS, JS)
- `requirements.txt` — dependensi Python
- `vercel.json` — konfigurasi deploy Vercel

## Lisensi
Gunakan bebas untuk belajar/percobaan.

