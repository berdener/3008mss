# Railway Dağıtım Talimatı

## 1) Ortam Değişkenleri
- `DATABASE_URL` → Railway PostgreSQL bağlantısı (ör: `postgresql://user:pass@host:port/db`)
- `SHOPIFY_STORE`, `SHOPIFY_ACCESS_TOKEN`, `SHOPIFY_LOCATION_ID` (opsiyonel)

## 2) Deploy
- Projeyi Railway'e bağla (GitHub ya da direkt upload).
- **Seçenek A (önerilen)**: Dockerfile kullan → otomatik build.
- **Seçenek B**: Procfile ile (buildpack) → bu repoda `Procfile` var.

## 3) Çalıştırma
- Railway `PORT` atar; Procfile ve Dockerfile `0.0.0.0:$PORT` ile çalışır.

## 4) PDF ve Barkod
- Dosyalar kalıcı olmadığı için geçici dizine yazılıyor (`/tmp`). PDF indirilebilir ama kalıcı değil.
