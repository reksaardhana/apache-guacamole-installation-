# Langkah-langkah Instalasi Apache Guacamole

1. **Perbarui sistem**
   ```bash
   sudo apt update && sudo apt upgrade -y
2. **Instal dependensi**
   ```bash
   sudo apt install -y build-essential libcairo2-dev libjpeg62-turbo-dev \
   libpng-dev libtool-bin libossp-uuid-dev libavcodec-dev libavformat-dev \
   libswscale-dev libwebp-dev
3. **Instal Tomcat dan Guacamole**
   ```bash
   sudo apt install -y tomcat9
- *Unduh Guacamole dari situs resminya:*
   ```bash
   wget https://apache.org/dyn/closer.cgi? 
   action=download&filename=guacamole/1.4.0/binary/guacamole-server- 
   1.4.0.tar.gz
4. **Ekstrak dan pasang**
   ```bash
   tar -xvzf guacamole-server-1.4.0.tar.gz
   cd guacamole-server-1.4.0
   ./configure --with-init-dir=/etc/init.d
   make
   sudo make install
5. **Restart Tomcat**
    ```bash
    sudo systemctl restart tomcat9

*Catatan:* Pastikan untuk mengikuti langkah-langkah lebih lanjut di 
[Konfigurasi](CONFIGURATION.md).
