# 🚀 Otomasi LEMP Stack & WordPress Menggunakan Ansible

## 📌 Deskripsi Proyek

Proyek ini merupakan implementasi otomasi infrastruktur server menggunakan **Ansible** untuk melakukan instalasi dan konfigurasi LEMP Stack serta WordPress pada Ubuntu Server.

Proyek ini menggunakan pendekatan **Multi-Tier Architecture**, yaitu memisahkan Web Server dan Database Server ke dalam dua Virtual Machine (VM) yang berbeda.

Tujuan utama proyek ini adalah membangun infrastruktur web server yang terstruktur, efisien, mudah dikelola, dan dapat dikonfigurasi secara otomatis menggunakan Ansible Playbook.

## 🎯 Tujuan Proyek

1. Memahami konsep LEMP Stack pada lingkungan Linux.
2. Menerapkan virtualisasi menggunakan Vagrant dan VirtualBox.
3. Mengimplementasikan Ansible sebagai alat otomasi konfigurasi server.
4. Memisahkan Web Server dan Database Server menggunakan arsitektur Multi-Tier.
5. Melakukan instalasi Nginx dan PHP secara otomatis.
6. Melakukan instalasi dan konfigurasi MariaDB secara otomatis.
7. Melakukan deployment WordPress dan menghubungkannya dengan Database Server.

## 🏗️ Arsitektur Sistem

Proyek ini menggunakan dua VM Target dan satu Control Node.

```text
              CONTROL NODE
                 Ansible
                    |
          ---------------------
          |                   |
          v                   v
    VM 1 - WEB SERVER    VM 2 - DATABASE
       Ubuntu Server       Ubuntu Server
          |                   |
         Nginx              MariaDB
          |                   |
          PHP                 |
          |                   |
       WordPress  ----------> |
                  Koneksi DB
```

### Komponen Infrastruktur

| Komponen | Fungsi |
|---|---|
| Control Node | Mengendalikan konfigurasi server menggunakan Ansible |
| VM 1 - Web Server | Menjalankan Nginx, PHP, dan WordPress |
| VM 2 - Database Server | Menyimpan database WordPress menggunakan MariaDB |

## 🛠️ Teknologi yang Digunakan

- **Ubuntu Server** – Sistem operasi server.
- **Vagrant** – Mengelola pembuatan dan konfigurasi Virtual Machine.
- **Oracle VirtualBox** – Platform virtualisasi.
- **Ansible** – Otomasi instalasi dan konfigurasi server.
- **Nginx** – Web Server.
- **PHP** – Bahasa pemrograman backend WordPress.
- **MariaDB** – Sistem manajemen basis data.
- **WordPress** – Content Management System (CMS).

## ⚙️ Implementasi Proyek

Proyek ini memiliki beberapa tahapan pengerjaan:

### 1. Persiapan Infrastruktur
- Instalasi Vagrant dan VirtualBox.
- Menyiapkan Ubuntu Server.
- Membuat dua Virtual Machine menggunakan Vagrant.
- Mengatur jaringan dan alamat IP setiap VM.

### 2. Konfigurasi Control Node
- Menyiapkan lingkungan Ansible.
- Mengatur koneksi SSH menuju VM Target.
- Membuat inventory Ansible.

### 3. Konfigurasi Web Server
- Instalasi Nginx.
- Instalasi PHP dan PHP-FPM.
- Konfigurasi Nginx untuk WordPress.
- Mengunduh dan mengekstrak WordPress.

### 4. Konfigurasi Database Server
- Instalasi MariaDB.
- Membuat database WordPress.
- Membuat user dan password database.
- Mengatur akses database dari Web Server.

### 5. Deployment WordPress
- Mengatur file konfigurasi `wp-config.php`.
- Menghubungkan WordPress dengan MariaDB.
- Melakukan pengujian akses WordPress melalui browser.

## 📁 Struktur Direktori Proyek

Struktur berikut merupakan rancangan direktori yang akan digunakan:

```text
otomasi-lemp-stack-wordpress-ansible/
│
├── Vagrantfile
│
├── inventory/
│   └── hosts
│
├── playbooks/
│   ├── site.yml
│   ├── webserver.yml
│   └── database.yml
│
├── roles/
│   ├── nginx/
│   ├── php/
│   ├── mariadb/
│   └── wordpress/
│
├── files/
│
├── screenshots/
│
└── README.md
```

## 🧪 Pengujian Sistem

Pengujian dilakukan untuk memastikan seluruh komponen dapat berjalan sesuai fungsinya.

Beberapa pengujian yang direncanakan:

- Memastikan Nginx berjalan pada VM Web Server.
- Memastikan PHP dapat diproses oleh Nginx.
- Memastikan MariaDB berjalan pada VM Database Server.
- Memastikan koneksi antara Web Server dan Database Server berhasil.
- Memastikan halaman instalasi WordPress dapat diakses melalui browser.

## 📚 Hasil yang Diharapkan

Melalui proyek ini, diharapkan dapat dibangun sebuah infrastruktur web server berbasis LEMP Stack dengan proses instalasi dan konfigurasi otomatis menggunakan Ansible.

Pemisahan Web Server dan Database Server diharapkan dapat meningkatkan pengelolaan sumber daya, keamanan, dan kemudahan pemeliharaan sistem.

## 👨‍💻 Identitas Proyek

- **Nama Proyek:** Otomasi LEMP Stack & WordPress
- **Mata Kuliah:** (Isi nama mata kuliah)
- **Metode:** Infrastructure Automation
- **Tools:** Vagrant, VirtualBox, Ansible
- **Platform:** Ubuntu Server

## 📌 Status Pengerjaan

Proyek ini dikembangkan secara bertahap sebagai bagian dari tugas proyek perkuliahan.

**Repository ini digunakan sebagai dokumentasi kode, konfigurasi, dan hasil implementasi proyek.**

---

⭐ *Developed for learning Linux Server Administration, Infrastructure Automation, and Web Server Deployment.*
