**CONFIGURATION.md**
File ini menjelaskan langkah-langkah konfigurasi.

# Konfigurasi Apache Guacamole

1. **Pengaturan database**
   - Buat database untuk Guacamole dan pengguna:
   ```sql
   CREATE DATABASE guacamole_db;
   CREATE USER 'guacamole_user'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON guacamole_db.* TO 'guacamole_user'@'localhost';
   FLUSH PRIVILEGES;
2. **Impor skema database**
   ```bash
   cat guacamole-auth-jdbc-1.4.0/mysql/schema/*.sql | mysql -u 
   guacamole_user -p guacamole_db
3. **Edit file konfigurasi Guacamole**
   - Sesuaikan dengan koneksi database Anda di
   ```bash
   /etc/guacamole/guacamole.properties
4. **Restart layanan**
   ```bash
   sudo systemctl restart tomcat9
