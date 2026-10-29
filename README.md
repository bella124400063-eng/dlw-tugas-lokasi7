# Studi Ablasi RNN, LSTM, GRU vs ANN untuk Prediksi Trafik Seluler Milan

Tugas Workshop Deep Learning — Teknik Telekomunikasi ITERA.

<!-- Ganti seluruh isian bertanda [ ... ] di bawah. Hapus komentar ini. -->

## Kelompok

| Peran | Nama | NIM |
|---|---|---|
| Ketua | [Bella Rizki Amalia] | [124400063] |
| Anggota | [Chelsy Enix Zeanventa] | [124400093] |
| Anggota | [Fella Putri Ardhia] | [124400007] |

- **Kelas:** [RA]
- **Lokasi kelompok:** [0] — [Università Bicocca] (digit terakhir NIM terkecil)
- **Laporan:** [`laporan-latex/main.pdf`]

## Cara Menjalankan

```bash
uv sync
uv run jupyter lab
```

Buka `tugas_ablasi.ipynb`, isi `LOKASI_KELOMPOK`, lalu jalankan semua sel. Semua run tercatat di `hasil/ablasi.csv`.

Perangkat yang kami pakai: [Perangkat yang kami pakai: Laptop (Intel Core i3-8145U / Intel Core i3-1215U / AMD Ryzen 5 7520U) dan Google Colab T4 GPU], total waktu training: [67,5] menit.

## Ringkasan Hasil
Eksperimen ablasi menunjukkan bahwa model rekuren (RNN dan GRU) secara konsisten mengungguli baseline ANN dalam memprediksi trafik seluler per jam. Pada area Duomo, model RNN mencapai Test MAE terbaik sebesar 229,60 ± 5,05, disusul oleh GRU (237,16 ± 9,32), LSTM (273,56 ± 25,36), dan ANN (314,28 ± 10,45). Pengujian generalisasi pada Lokasi 7 (Università Bicocca) mengonfirmasi kestabilan hierarki model dengan Test MAE terbaik dicapai oleh RNN sebesar 47,83 ± 2,86.

## Struktur

```
tugas_ablasi.ipynb      notebook eksperimen (di-commit beserta output)
data/                   data trafik per jam (Duomo + 10 lokasi tugas)
hasil/                  CSV seluruh run, tabel, dan grafik
laporan-latex/ atau laporan-typst/   sumber laporan + PDF
```

## Data

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).
