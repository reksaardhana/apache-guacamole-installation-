**CONFIGURATION.md**
File ini menjelaskan langkah-langkah konfigurasi.

```markdown
# Konfigurasi Apache Guacamole
```

1. **Pengaturan database**
   - Buat database untuk Guacamole dan pengguna:
   ```sql
   CREATE DATABASE guacamole_db;
   CREATE USER 'guacamole_user'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON guacamole_db.* TO 'guacamole_user'@'localhost';
   FLUSH PRIVILEGES;
