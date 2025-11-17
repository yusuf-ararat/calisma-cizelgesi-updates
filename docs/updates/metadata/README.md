# TUF Metadata Dizini

Bu dizin, TUF (The Update Framework) metadata dosyalarını içerir ve GitHub Pages üzerinden sunulur.

## Dosyalar

- **root.json**: Root metadata, public key bilgilerini içerir
- **targets.json**: Hedef dosyaların (EXE, patch) bilgileri
- **snapshot.json**: Metadata versiyonlarının snapshot'ı
- **timestamp.json**: En güncel metadata versiyonu
- **.nojekyll**: GitHub Pages'in Jekyll işlemini bypass eder

## URL

Production'da bu dizin şu URL'den erişilebilir olacak:
```
https://[username].github.io/calisma-cizelgesi-v0/updates/metadata/
```

## Güncelleme Akışı

1. Yeni release yayınlandığında GitHub Actions otomatik tetiklenir
2. `build/generate_tuf_metadata.py` script'i çalışır
3. Metadata dosyaları güncellenir ve imzalanır
4. Değişiklikler bu dizine commit edilir
5. GitHub Pages otomatik deploy edilir

## Güvenlik

- Tüm metadata dosyaları Ed25519 ile dijital olarak imzalanır
- Private key GitHub Secrets'ta saklanır
- HTTPS zorunludur

## Test

Local test için Python HTTP server kullanabilirsiniz:
```bash
cd docs
python -m http.server 8000
# Metadata URL: http://localhost:8000/updates/metadata/
```

## Notlar

- Bu dizindeki dosyalar otomatik oluşturulur
- Manuel değişiklik yapmayın
- GitHub Actions tarafından yönetilir
