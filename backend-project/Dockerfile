# Gunakan image dasar yang sesuai, misalnya Debian atau Alpine
FROM alpine:3.16

# Install dependensi yang diperlukan
RUN apk update && apk add nginx

# Salin file konfigurasi nginx (sesuaikan path jika perlu)
COPY nginx-backend.conf /etc/nginx/conf.d/default.conf

# Salin file konfigurasi Prometheus jika diperlukan
COPY prometheus.yml /etc/prometheus/prometheus.yml

# Salin konten website jika Anda menyertakan website statis
COPY website/ /usr/share/nginx/html

# Expose port yang akan digunakan
EXPOSE 80

# Jalankan perintah untuk memulai nginx di foreground
CMD ["nginx", "-g", "daemon off;"]
