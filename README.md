# Çalışma Çizelgesi - Güncelleme Sunucusu

Bu repository, **Personel Çizelgesi Yönetim Sistemi** uygulamasının otomatik güncelleme metadata dosyalarını barındırır.

## Amaç

Ana uygulama kodları private repository'de tutulurken, güncelleme sistemi için gerekli metadata dosyaları bu public repository üzerinden GitHub Pages ile sunulur.

## Yapı

```
docs/
└── updates/
    └── metadata/
        ├── root.json      # Ana güvenlik dosyası
        ├── targets.json   # Güncelleme hedefleri
        ├── snapshot.json  # Versiyon bilgileri
        └── timestamp.json # Son güncelleme zamanı
```

## Güvenlik

- Bu repository sadece metadata içerir
- Gerçek uygulama dosyaları private repository'de korunur
- Tüm metadata dosyaları dijital olarak imzalanmıştır

## GitHub Pages URL

Aktif olduktan sonra:
```
https://yusuf-ararat.github.io/calisma-cizelgesi-updates/updates/metadata/
```

## Ana Proje

Ana proje (private): https://github.com/yusuf-ararat/calisma-cizelgesi-v0

---

*Bu repository otomatik güncelleme sistemi için oluşturulmuştur.*