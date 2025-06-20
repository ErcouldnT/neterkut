# 📡 neterkut

## İçindekiler / Table of Contents
- [English](#-english-instructions)
- [Türkçe](#-türkçe-açıklama)

---

## 🇬🇧 English Instructions

### 🔧 Services

#### 1. Tailscale
- Provides secure mesh networking.
- DNS forwarding is disabled via `--accept-dns=false`.

#### 2. DNSCrypt Proxy
- Encrypts DNS queries.
- Acts as an upstream DNS server for Pi-hole.

#### 3. Pi-hole
- Blocks ads, trackers, and malicious domains.
- Uses DNSCrypt as its upstream resolver.
- Accessible over Tailscale network remotely.

### 📁 Folder Structure

```
project-root/
├── docker-compose.yaml
├── .env
├── tailscale-data/
├── dnscrypt/
├── etc-pihole/
└── etc-dnsmasq.d/
```

### 🚀 Setup

1. Create `.env` file:

```env
TS_AUTHKEY=tskey-xxxxxxxxxxxxxx
PIHOLE_PASSWORD=your-secret-password
```

2. Edit `dnscrypt/dnscrypt-proxy.toml` if needed.

3. Start services:

```bash
docker compose up -d
```

### 🛠️ Notes

- Access Pi-hole UI: `http://100.x.x.x/admin`

---

## 🇹🇷 Türkçe Açıklama

### 🔧 Servisler

#### 1. Tailscale
- Özel ağ üzerinden güvenli bağlantı sağlar.
- `--accept-dns=false` ile DNS yönlendirmesi kapalıdır.

#### 2. DNSCrypt Proxy
- DNS sorgularını şifreler.
- Pi-hole’a upstream DNS olarak hizmet eder.

#### 3. Pi-hole
- Reklam, izleyici ve zararlı alan adlarını engeller.
- DNSCrypt üzerinden DNS sorgularını işler.
- Tailscale ağı sayesinde uzaktan erişim mümkündür.

### 📁 Klasör Yapısı

```
proje-dizini/
├── docker-compose.yaml
├── .env
├── tailscale-data/
├── dnscrypt/
├── etc-pihole/
└── etc-dnsmasq.d/
```

### 🚀 Kurulum

1. `.env` dosyasını oluştur:

```env
TS_AUTHKEY=tskey-xxxxxxxxxxxxxx
PIHOLE_PASSWORD=your-secret-password
```

2. Gerekirse `dnscrypt/dnscrypt-proxy.toml` dosyasını düzenle.

3. Servisleri başlat:

```bash
docker compose up -d
```

### 🛠️ Notlar

- Pi-hole arayüzü: `http://100.x.x.x/admin`

