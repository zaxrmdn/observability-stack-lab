# Practical Linux Server Monitoring & Observability Workshop Lab

Repositori ini berisi panduan praktikum mandiri dan berkas konfigurasi siap pakai untuk membangun **Full-Stack Observability** (Metrik, Log, dan Alerting) pada server Linux menggunakan Docker Compose. 

Infrastruktur monitoring ini didesain ringkas dan cepat agar dapat diselesaikan dalam sesi workshop berdurasi 4 jam.

---

## Arsitektur Monitoring Stack

Lab ini menggabungkan 5 komponen utama yang saling terintegrasi:
1. **Node Exporter:** Agen pengumpul data metrik internal sistem operasi Linux host.
2. **Prometheus (TSDB):** Database berbasis waktu yang bertugas menarik (*scraping*) dan menyimpan data metrik secara berkala.
3. **Loki:** Database terpusat khusus untuk menampung data log sistem dengan efisiensi tinggi.
4. **Promtail:** Agen kurir log yang membaca file `/var/log/*.log` pada host dan mengirimkannya ke Loki.
5. **Grafana:** Pusat kendali visual (*Single Pane of Glass*) untuk menampilkan grafik metrik dan teks log secara terpadu.

---

## Persyaratan Sistem (Prerequisites)

Sebelum memulai, pastikan lingkungan kerja Anda memenuhi kriteria berikut:
* **OS:** Linux (Ubuntu 20.04/22.04 LTS sangat disarankan), macOS, atau Windows dengan WSL2.
* **Hardware:** Minimal 2 Core CPU, 4 GB RAM, dan 10 GB sisa penyimpanan.
* **Software:** Docker Engine dan Docker Compose v2.0+ telah terinstal.
* **Akses:** Hak akses untuk menjalankan perintah `sudo` di terminal.

---
