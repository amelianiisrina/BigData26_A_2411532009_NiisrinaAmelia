# Kamus Data Dataset Akhir

| Nama Kolom | Tipe | Satuan | Sumber | Aturan Validitas | Penanganan Nilai Hilang |
|---|---|---|---|---|---|
| `tpep_pickup_datetime` | datetime64[us] | waktu | TLC Trip Data | waktu pickup valid | Tidak ada |
| `tpep_dropoff_datetime` | datetime64[us] | waktu | TLC Trip Data | waktu dropoff valid | Tidak ada |
| `passenger_count` | float64 | penumpang | TLC Trip Data | tidak kosong | Median per jam |
| `trip_distance` | float64 | mil | TLC Trip Data | 0,01–100 mil | Baris tidak valid dihapus |
| `PULocationID` | int64 | ID zona | TLC Trip Data | ID zona dikenal | Tidak ada |
| `DOLocationID` | int64 | ID zona | TLC Trip Data | ID zona valid | Tidak ada |
| `payment_type` | int64 | kode | TLC Trip Data | Kode pembayaran valid | Tidak ada |
| `fare_amount` | float64 | USD | TLC Trip Data | Nilai numerik | Tidak ada |
| `tip_amount` | float64 | USD | TLC Trip Data | Nilai numerik | Tidak ada |
| `total_amount` | float64 | USD | TLC Trip Data | > 0 dan ≥ fare_amount | Baris tidak valid dihapus |
| `durasi_menit` | float64 | menit | Hasil transformasi | 1–180 menit | Baris tidak valid dihapus |
| `jam` | int32 | jam | Hasil transformasi | 0–23 | Tidak ada |
| `borough_naik` | object | - | Data zona | Sesuai PULocationID | Missing dibiarkan |
| `nama_pembayaran` | object | - | Referensi pembayaran | Sesuai payment_type | Missing dibiarkan |
| `jam_mulai` | datetime64[us] | waktu | Hasil transformasi | Dibulatkan ke jam | Tidak ada |
| `suhu_c` | float64 | °C | Open-Meteo Weather API | Nilai numerik | Missing dibiarkan |
| `hujan_mm` | float64 | mm | Open-Meteo Weather API | ≥ 0 | Missing dibiarkan |
| `tanggal` | object | tanggal | Hasil transformasi | Format tanggal valid | Tidak ada |