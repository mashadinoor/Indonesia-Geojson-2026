# 🗺️ GeoJSON Indonesia — 38 Provinsi

> Fork dari [ardian28/GeoJson-Indonesia-38-Provinsi](https://github.com/ardian28/GeoJson-Indonesia-38-Provinsi) dengan perbaikan data dan restrukturisasi folder.

---

## 📁 Struktur

```
├── 📂 Provinsi/
│   ├── Aceh.json
│   ├── Bali.json
│   └── ...  (38 file)
└── 📂 Kabupaten/
    ├── 📂 Aceh/
    │   ├── Kabupaten_Aceh_Barat.json
    │   ├── Kabupaten_Aceh_Besar.json
    │   └── ...
    ├── 📂 Bali/
    │   ├── Kabupaten_Badung.json
    │   ├── Kota_Denpasar.json
    │   └── ...
    └── ...  (38 subfolder)
```

Setiap file adalah GeoJSON valid dengan format:

```json
{
  "type": "FeatureCollection",
  "features": [ ... ]
}
```

---

## ✨ Perubahan dari repo asli

### 🔧 Fix: `KODE_PROV` duplikat provinsi Papua

Repo asli memiliki `KODE_PROV` yang duplikat untuk 6 provinsi hasil pemekaran Papua. Telah diperbaiki sesuai **Kepmendagri No. 100.1.1-6117 Tahun 2022**:

| Provinsi         |   Sebelum   |  Sesudah  |
| ---------------- | :---------: | :-------: |
| Papua            | ❌ duplikat | ✅ **91** |
| Papua Barat      | ❌ duplikat | ✅ **92** |
| Papua Selatan    | ❌ duplikat | ✅ **93** |
| Papua Tengah     | ❌ duplikat | ✅ **94** |
| Papua Pegunungan | ❌ duplikat | ✅ **95** |
| Papua Barat Daya | ❌ duplikat | ✅ **96** |

📎 Referensi: [Provinsi di Indonesia — Wikipedia](https://id.wikipedia.org/wiki/Provinsi_di_Indonesia)

### 📂 Restrukturisasi folder

- **Provinsi** → satu file `.json` per provinsi
- **Kabupaten** → subfolder per provinsi, satu file per kabupaten/kota dengan prefix `Kabupaten_` atau `Kota_`

---

## 🗃️ Sumber Data

| Sumber                                                                                                                                       | Keterangan            |
| -------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| [Badan Informasi Geospasial (BIG)](https://geoservice.big.go.id)                                                                             | Data geometri wilayah |
| [Kepmendagri No. 100.1.1-6117 Tahun 2022](https://upload.wikimedia.org/wikipedia/commons/9/93/Kepmendagri_Nomor_100.1.1-6117_Tahun_2022.pdf) | Kode wilayah resmi    |

---

## 🤝 Berkontribusi

Kontribusi sangat disambut! Jika kamu menemukan data yang tidak akurat, kode wilayah yang salah, atau ingin menambahkan peningkatan lainnya:

1. **Laporkan issue** — Temukan kesalahan data atau bug? Buka [Issue baru](../../issues/new) dan jelaskan masalahnya sedetail mungkin.
2. **Ajukan perubahan** — Fork repo ini, buat perubahan, lalu buka Pull Request.
3. **Diskusi** — Punya ide atau pertanyaan? Gunakan tab [Discussions](../../discussions) untuk berdiskusi.

Beberapa hal yang bisa dikontribusikan:

- 🐛 Fix data geometri yang tidak akurat
- 🏷️ Koreksi nama atau kode wilayah
- 📝 Perbaikan dokumentasi
- ⭐ Ide fitur atau struktur data baru

---

## 📄 Lisensi

MIT — sama dengan repo asli. Kredit ke [ardian28](https://github.com/ardian28).
