Berikut adalah **perintah-perintah dasar terminal Linux** yang perlu diketahui, dikelompokkan berdasarkan fungsi:

## 📁 **Navigasi & Manajemen File**
```bash
pwd                 # Tampilkan direktori saat ini
ls                  # List isi direktori
ls -l              # List detail (permission, ukuran)
ls -a              # List semua file (termasuk hidden)
cd <folder>        # Pindah direktori
cd ..              # Kembali ke direktori parent
cd ~               # Ke home directory
cd /               # Ke root directory
```

## 📄 **Manipulasi File**
```bash
touch file.txt     # Buat file baru
mkdir folder       # Buat direktori baru
cp file1 file2     # Salin file
cp -r dir1 dir2    # Salin direktori rekursif
mv file1 file2     # Pindah/rename file
rm file.txt        # Hapus file
rm -r folder       # Hapus direktori rekursif
rm -rf folder      # Hapus paksa (hati-hati!)
```

## 👀 **Melihat Isi File**
```bash
cat file.txt       # Tampilkan seluruh konten
less file.txt      # Tampilan halaman per halaman
head file.txt      # 10 baris pertama
tail file.txt      # 10 baris terakhir
tail -f log.txt    # Pantau file real-time (untuk log)
```

## 🔍 **Pencarian**
```bash
find /path -name "*.txt"  # Cari file
grep "pattern" file.txt   # Cari teks dalam file
grep -r "pattern" /path  # Cari rekursif
locate file.txt          # Cari menggunakan database
which command           # Tampilkan path executable
whereis command        # Tampilkan lokasi binary, source, manual
```

## 📦 **Manajemen Proses**
```bash
ps                   # Tampilkan proses aktif
ps aux              # Tampilkan semua proses detail
top                 # Monitor proses real-time
htop                # Versi improved dari top
kill PID            # Hentikan proses
kill -9 PID         # Hentikan paksa
bg                  # Jalankan proses di background
fg                  # Bawa ke foreground
jobs                # List jobs background
```

## 🛠️ **System Info & Monitoring**
```bash
uname -a            # Info kernel
whoami              # User saat ini
hostname            # Nama host
df -h               # Disk usage (human readable)
du -sh folder       # Ukuran folder
free -h             # Memory usage
uptime              # Waktu sistem aktif
history             # Riwayat perintah
```

## 🔐 **Permissions & Ownership**
```bash
chmod 755 file      # Ubah permission file
chmod +x script.sh  # Jadikan executable
chown user:group file  # Ubah owner dan group
sudo command        # Jalankan sebagai superuser
su                  # Switch user
passwd              # Ganti password
```

## 🌐 **Network**
```bash
ping google.com     # Test koneksi
ifconfig / ip a     # Info network interface
curl url            # Transfer data dari URL
wget url            # Download file
ssh user@host       # Koneksi SSH
scp file user@host:path  # Copy file via SSH
netstat -tulpn     # Koneksi network aktif
```

## **Package Management**
### Debian/Ubuntu (APT)
```bash
sudo apt update     # Update package list
sudo apt upgrade    # Upgrade packages
sudo apt install package  # Install package
sudo apt remove package   # Uninstall package
```

### RHEL/CentOS (YUM/DNF)
```bash
sudo yum install package
sudo dnf install package  # Versi lebih baru
```

## **Archive & Compression**
```bash
tar -czvf archive.tar.gz folder/  # Buat archive
tar -xzvf archive.tar.gz          # Extract archive
zip archive.zip file              # Buat zip
unzip archive.zip                 # Extract zip
gzip file                         # Kompresi gzip
gunzip file.gz                    # Decompress gzip
```

## **Editor Teks (dalam terminal)**
```bash
nano file.txt       # Editor sederhana
vim file.txt        # Editor advanced
gedit file.txt      # GUI editor (jika tersedia)
```

## **Tips Penting**
1. **Auto-complete**: Tekan `Tab` untuk melengkapi perintah/nama file
2. **Riwayat**: Tekan `↑`/`↓` untuk navigasi history
3. **Clear screen**: `Ctrl + L` atau `clear`
4. **Cancel process**: `Ctrl + C`
5. **Exit terminal**: `Ctrl + D` atau `exit`

## ⚠️ **Perintah Berbahaya (Hati-hati!)**
```bash
rm -rf /            # Hapus seluruh sistem!
dd if=/dev/zero of=/dev/sda  # Hapus disk!
:(){ :|:& };:       # Fork bomb (DoS)
```

## **Contoh Kombinasi Berguna**
```bash
ls -la | grep ".txt"           # Cari file .txt
cat file.txt | wc -l           # Hitung baris
ps aux | grep process_name     # Cari proses
find . -name "*.log" -exec rm {} \;  # Hapus semua file log
```

**Tips**: Gunakan `man <command>` untuk melihat manual lengkap suatu perintah, contoh: `man ls`
