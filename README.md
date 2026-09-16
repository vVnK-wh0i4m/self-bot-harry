<div align="center">

# ⚡ Self Bot Harry ⚡

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Discord.py](https://img.shields.io/badge/Discord.py--self-2.0%2B-purple?logo=discord&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Version](https://img.shields.io/badge/Version-Remakable-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Download](https://img.shields.io/badge/Download-Zip-blue?style=for-the-badge&logo=github)

**Discord Self Bot với 4 tính năng: Spam, Nhây, Nhây Fake Typing, Réo tên - Multi-token, Multi-channel, Rate limit handling.**

[📥 **Tải code (.zip)**](https://github.com/vVnK-wh0i4m/self-bot-harry/archive/refs/heads/main.zip) • [📦 **Clone repo**](https://github.com/vVnK-wh0i4m/self-bot-harry.git)

</div>

---

## ⚠️ Cảnh báo quan trọng

> **Công cụ này được cung cấp cho mục đích giải trí, thử nghiệm và nghiên cứu.** Người dùng **chịu toàn bộ trách nhiệm** khi sử dụng. **KHÔNG** sử dụng cho mục đích vi phạm pháp luật hoặc gây hại đến người khác.

> **Sử dụng self-bot vi phạm [Discord Terms of Service](https://discord.com/terms).** Tài khoản của bạn **có thể bị khóa vĩnh viễn**.

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Yêu cầu hệ thống](#-yêu-cầu-hệ-thống)
- [Cài đặt và chạy](#-cài-đặt-và-chạy)
- [Cách sử dụng](#-cách-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Hướng dẫn chi tiết](#-hướng-dẫn-chi-tiết)
- [FAQ](#-câu-hỏi-thường-gặp)
- [Bản quyền](#-bản-quyền)

---

## 🌟 Giới thiệu

**Self Bot Harry** là Discord Self Bot Python được xây dựng bằng **aiohttp** và **asyncio** với giao diện console màu sắc, hỗ trợ multi-token và multi-channel. Tool cung cấp 4 tính năng chính với rate limit handling tự động.

**Điểm nổi bật:**
- 🎯 4 chế độ: Spam, Nhây, Nhây Fake Typing, Réo tên
- 🔀 Multi-token - load từ file, validate tự động
- 📡 Multi-channel - chạy song song nhiều kênh
- ⏱️ Rate limit handling - tự retry khi bị limit
- 🎨 Giao diện console màu sắc với ASCII art

---

## 🚀 Tính năng

### 📨 Chế độ 1: Spam

| Tính năng | Mô tả |
|-----------|--------|
| Spam tin nhắn | Gửi tin nhắn liên tục vào kênh |
| Multi-token | Nhiều token chạy song song |
| Delay tùy chỉnh | Delay giữa mỗi tin nhắn |
| Auto retry | Tự retry khi bị rate limit |

### 💬 Chế độ 2: Nhây

| Tính năng | Mô tả |
|-----------|--------|
| Nhây | Spam nhiều tin nhắn khác nhau từ file |
| Tag người dùng | Chọn tag hoặc không tag |
| Multi-line | Mỗi dòng là 1 tin nhắn |

### ⌨️ Chế độ 3: Nhây Fake Typing

| Tính năng | Mô tả |
|-----------|--------|
| Fake typing | Giả lập đang soạn tin nhắn |
| Hiệu ứng gõ chữ | Hiển thị từng ký tự trên console |
| Auto send | Gửi sau khi "gõ" xong |

### 📢 Chế độ 4: Réo tên

| Tính năng | Mô tả |
|-----------|--------|
| Réo tên | Nhập tên cần réo, thay `{name}` trong tin nhắn |
| Fake typing | Giả lập soạn tin nhắn |
| Tag + tên | Kết hợp tag người dùng và réo tên |

---

## 💻 Yêu cầu hệ thống

| Thành phần | Yêu cầu |
|------------|----------|
| Python | 3.8 trở lên |
| RAM | Tối thiểu 512MB |
| Mạng | Kết nối internet ổn định |

---

## 📥 Cài đặt và chạy

### Bước 1: Clone repo

```bash
git clone https://github.com/vVnK-wh0i4m/self-bot-harry.git
cd self-bot-harry
```

### Bước 2: Tạo virtual environment (khuyến nghị)

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### Bước 3: Cài đặt thư viện

```bash
pip install -r requirements.txt
```

### Bước 4: Chuẩn bị file

**1. File token (`tokens.txt`):**
```
MTQ2ODIzOTA1NzM1MDk1NTA5OQ.G1xxxxx.xxxxxxxxxxxxxxxxxxxxxxxx
OTc4NTIwNzIxMjAxMDAwMjYw.YOUR_TOKEN_HERE.xxxxxxxxxxxxxxxxxxxxxxxx
```

**2. File nội dung (`ngon.txt` hoặc `nhay.txt`):**
```
Xin chào các bạn!
Hôm nay trời đẹp quá!
AIFAOIHFASIOFHASIOFH
```

### Bước 5: Chạy tool

```bash
python bot.py
```

---

## 📖 Cách sử dụng

### Menu chính

```
Chọn chức năng (1: Spam, 2: Nhây, 3: Nhây Fake Typing, 4: Réo Tên): 
```

### Chế độ 1: Spam

```
1. Nhập ID kênh: 1234567890
2. Tên file token cho kênh: tokens.txt
3. Chọn file chứa tin nhắn: 1
4. Nhập delay cho token thứ 1: 2.5
```

### Chế độ 2: Nhây

```
1. Có muốn tag người dùng không? (y/n): y
2. Nhập ID người cần tag: 1111111111,2222222222
3. Nhập ID kênh: 1234567890
4. Tên file token cho kênh: tokens.txt
5. Chọn file chứa tin nhắn: 1
6. Nhập delay cho token thứ 1: 1.5
```

### Chế độ 3: Nhây Fake Typing

```
1. Có muốn tag người dùng không? (y/n): n
2. Nhập ID kênh: 1234567890
3. Tên file token cho kênh: tokens.txt
4. Chọn file chứa tin nhắn: 1
5. Nhập delay cho token thứ 1: 2.0
```

### Chế độ 4: Réo tên

```
1. Có muốn tag người dùng không? (y/n): y
2. Nhập ID người cần tag: 1111111111
3. Nhập tên cần réo: Anh Ba
4. Nhập ID kênh: 1234567890
5. Tên file token cho kênh: tokens.txt
6. Chọn file chứa tin nhắn: 1
7. Nhập delay cho token thứ 1: 1.5
```

> Tin nhắn phải chứa `{name}` để thay tên. Ví dụ: `Ê {name}, mày đâu rồi?`

---

## 📁 Cấu trúc dự án

```
self-bot-harry/
├── bot.py              # Code chính
├── ngon.txt            # Nội dung spam/nhây
├── nhay.txt            # Nội dung nhây
├── requirements.txt    # Dependencies
├── app.log             # Log output
├── .gitignore
├── LICENSE
└── README.md
```

---

## 📖 Hướng dẫn chi tiết

### File token

File chứa Discord User Token, mỗi token 1 dòng:

```
TOKEN_1
TOKEN_2
TOKEN_3
```

**Cách lấy User Token:**
1. Mở Discord trên trình duyệt (browser)
2. F12 → Network → Gửi tin nhắn bất kỳ
3. Tìm request → Headers → Authorization
4. Copy giá trị Authorization (không có `Bot ` hay `Bearer `)

### File nội dung

- `ngon.txt`: Nội dung spam/nhây (mỗi dòng 1 tin nhắn)
- `nhay.txt`: Nội dung nhây (mỗi dòng 1 tin nhắn)

### Delay

- Delay tính bằng giây (có thể dùng số thập phân)
- Ví dụ: `1.5` = 1.5 giây giữa mỗi tin nhắn
- Tool sẽ thêm random 0.5-1.5 giây nữa để tránh bị detect

### Multi-channel

- Có thể nhập nhiều ID kênh
- Mỗi kênh cần file token riêng
- Tool chạy song song tất cả kênh

---

## ❓ Câu hỏi thường gặp

### Tool cần Python version nào?

Python 3.8 trở lên. Kiểm tra: `python --version`

### Lỗi `ModuleNotFoundError`?

Chạy: `pip install -r requirements.txt`

### Token không hoạt động?

1. Kiểm tra token có đúng format không
2. Token có thể đã bị invalid → lấy token mới
3. Kiểm tra `app.log` để xem lỗi chi tiết

### Bị rate limit (429)?

Tool tự retry khi bị rate limit. Nếu liên tục bị:
- Tăng delay lên
- Giảm số token chạy cùng lúc
- Chỉ chạy 1 channel tại 1 thời điểm

### Tin nhắn bị cắt?

Discord giới hạn 2000 ký tự/tin nhắn. Tool sẽ tự cắt nếu quá dài.

---

## 📜 Bản quyền

**MIT License** - Xem file [LICENSE](LICENSE) để biết chi tiết.

Điều khoản sử dụng:

| ✅ Được phép | ❌ Không được phép |
|-------------|-------------------|
| Giải trí cá nhân | Quấy rối người khác |
| Nghiên cứu, học tập | Spam, gây phiền |
| Thử nghiệm | Vi phạm pháp luật |

---

<div align="center">

**⭐ Star repo nếu thấy hữu ích! ⭐**

Made with ❤️ by Harry

</div>
