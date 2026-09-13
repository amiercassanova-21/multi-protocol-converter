<div align="center">

# ⚡ CASSANOVA
### Universal Protocol to JSON Converter
**High-Performance Xray / V2Ray Core Config Generator**

[![Live Web App](https://img.shields.io/badge/Website-multi.cassanova.my.id-eab308?style=for-the-badge&logo=googlechrome&logoColor=020611)](https://multi.cassanova.my.id/)
[![Engine Version](https://img.shields.io/badge/Core Engine-V3.8-38bdf8?style=for-the-badge&logo=xray)](https://multi.cassanova.my.id/)
[![Telegram Contact](https://img.shields.io/badge/Telegram-@kang__rebahan-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/kang_rebahan)
[![WhatsApp Contact](https://img.shields.io/badge/WhatsApp-Chat_Owner-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.link/3yhb8f)

<p align="center">
  <b>Aplikasi Web Ultra-Modern untuk Mengonversi Link Akun VLESS, VMess, & Trojan Menjadi Konfigurasi JSON Teroptimasi 100% SiapPakai di v2rayNG / v2rayN.</b>
</p>

---

</div>

## 📌 Tentang JSON Converter

**CASSANOVA Universal Protocol to JSON Converter** adalah platform web generasi baru yang dirancang untuk mengurai (*parse*) dan mengonversi link akun VPN berbasis protokol **VLESS**, **VMess**, dan **Trojan** secara otomatis menjadi struktur kode **JSON Xray/V2Ray Core**.

Konfigurasi yang dihasilkan telah melewati optimasi tingkat tinggi, sehingga ketika di-import ke aplikasi klien seperti **v2rayNG (Android)** atau **v2rayN (Windows)**, koneksi langsung aktif, ber-ping rendah (*low latency*), serta kebal dari kebocoran DNS (*Anti-DNS Leak*).

🌐 **Akses Web:** [https://multi.cassanova.my.id/](https://multi.cassanova.my.id/)

---

## ✨ Fitur Unggulan

- 🚀 **Auto-Detect Protocol Parsing**: Deteksi otomatis protokol `vless://`, `vmess://` (Base64 JSON), dan `trojan://` tanpa konfigurasi manual.
- 🛡️ **Pencegahan Kebocoran DNS (Anti-DNS Leak)**: Memakai arsitektur inbound `dokodemo-door` (port `10853`) yang meneruskan seluruh kueri DNS ke `dns-out`.
- ⚡ **Strategi IPv4 & DNS Fallback**: Menggunakan `queryStrategy: "UseIPv4"` serta DNS cadangan (`1.1.1.1` & `8.8.8.8`) untuk menghindari *delay handshake* di jaringan ISP lokal (Telkomsel, Indosat, XL, Tri, Smartfren, Biznet, dll).
- 📵 **Proteksi Anti-Torrent (DMCA Safe)**: Dilengkapi dengan aturan *routing* blokir otomatis untuk protokol `bittorrent` guna melindungi server VPS dari tindakan pembekuan (*suspend*).
- 🖥️ **Kompatibilitas Multi-Perangkat**: Menyediakan *Inbound Dual-Port* SOCKS (`10808`) untuk Android TUN/VPN Service dan HTTP (`10809`) untuk browser PC/Desktop.
- 🎨 **Antarmuka Cyber Luxury Obsidian UI**: Tampilan visual kelas atas berbasis *Glassmorphism*, fitur *Instant Telemetry Chips*, serta *IDE Code Viewer Window* yang responsif.
- 📋 **One-Click Action**: Mendukung aksi tempel cepat (*Paste*), salin instan (*Copy JSON*), serta unduh langsung file `.json`.

---

## 🛰️ Protokol & Transport Yang Didukung

| Parameter | Cakupan Dukungan |
| :--- | :--- |
| **Protokol** | `VLESS`, `VMess`, `Trojan` |
| **Port Utama** | Port `443` (TLS / Secure) & Port `80` (HTTP / Non-TLS) |
| **Mode Transport** | WebSocket (`ws`), gRPC (`grpc`), TCP |
| **Keamanan TLS** | SNI Auto-Extractor, Host Header Matching, Skip Insecure Checks |

---

## 🛠️ Cara Penggunaan

1. **Salin Link Akun**: Tempelkan link akun `vless://`, `vmess://`, atau `trojan://` yang Anda miliki.
2. **Buka Converter**: Akses [https://multi.cassanova.my.id/](https://multi.cassanova.my.id/).
3. **Tempel & Konversi**: Klik tombol **📋 Paste** lalu tekan **🚀 Konversi ke JSON Config**.
4. **Dapatkan JSON**:
   - Klik **📋 Salin JSON** untuk menempelkan isi konfigurasi ke aplikasi, atau
   - Klik **⬇️ Unduh .json** untuk menyimpan file `.json`.
5. **Import ke Aplikasi**: Buka **v2rayNG** / **v2rayN** -> *Import Config from Clipboard* / *Import Config File* -> Konek & Enjoy! ⚡

---

## 🏗️ Struktur Arsitektur JSON Output

Setiap keluaran JSON yang dihasilkan mengikuti struktur Xray/V2Ray Core berikut:

```json
{
  "log": { "loglevel": "warning" },
  "dns": {
    "servers": ["1.1.1.1", "8.8.8.8"],
    "queryStrategy": "UseIPv4"
  },
  "inbounds": [
    { "port": 10808, "protocol": "socks", "tag": "socks" },
    { "port": 10809, "protocol": "http", "tag": "http-in" },
    { "port": 10853, "protocol": "dokodemo-door", "tag": "dns-in" }
  ],
  "outbounds": [
    { "tag": "proxy", "protocol": "vless/vmess/trojan", ... },
    { "tag": "direct", "protocol": "freedom" },
    { "tag": "block", "protocol": "blackhole" },
    { "tag": "dns-out", "protocol": "dns" }
  ],
  "routing": {
    "domainStrategy": "IPIfNonMatch",
    "rules": [ ... ]
  }
}
```

---

## 👤 Pemilik & Pengembang

Aplikasi web ini dibangun dan dikembangkan sepenuhnya oleh **amiercassanova**.

- 🌐 **Official Web App:** [multi.cassanova.my.id](https://multi.cassanova.my.id/)
- 💬 **Telegram:** [@kang_rebahan](https://t.me/kang_rebahan)
- 📱 **WhatsApp:** [Hubungi via WhatsApp](https://wa.link/3yhb8f)

---

<div align="center">
  <sub>Developed with ❤️ by <b>amiercassanova</b> • Powered by Xray / V2Ray Core Architecture</sub>
</div>
