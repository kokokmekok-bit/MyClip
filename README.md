# AutoClip AI Online v1

Fitur: upload video, transkripsi bertimestamp, AI memilih 5 bagian menarik, potong otomatis 9:16, preview, download MP4 dan ZIP.

## Deploy Railway
1. Upload semua isi project ke repository GitHub.
2. Di Railway: New Project -> Deploy from GitHub Repo.
3. Pilih repository. Railway akan mendeteksi Dockerfile.
4. Buka Variables dan isi:
   OPENAI_API_KEY=sk-...
   OPENAI_TEXT_MODEL=gpt-5.6-luna
   OPENAI_TRANSCRIBE_MODEL=gpt-4o-mini-transcribe
   MAX_FILE_SIZE_MB=800
   CLIP_COUNT=5
5. Deploy / Redeploy.
6. Settings -> Networking -> Generate Domain.
7. Buka domain dari HP.

Catatan: jangan upload API key ke GitHub. Versi MVP menyimpan clip sementara di disk container; aplikasi publik sebaiknya memakai object storage dan job queue.
