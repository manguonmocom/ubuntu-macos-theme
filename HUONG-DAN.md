# Theme macOS cho Ubuntu — Hướng dẫn (Tiếng Việt)

Cài **giao diện giống macOS trên Ubuntu** với **MacTahoe**: theme, Dock kiểu Mac, Widgets desktop, và tuỳ chọn bộ gõ **Ngó Sen** — quản lý hàng ngày bằng **MacTahoe Control**.

**Từ khóa:** theme macOS Ubuntu · làm Ubuntu giống Mac · MacTahoe · Dock GNOME · Ubuntu 20.04 22.04 24.04 · giao diện macOS Linux

---

## Phiên bản Ubuntu được hỗ trợ

| Phiên bản | Theme / icon | Dock + Widgets | Ngó Sen | Ghi chú |
|-----------|--------------|----------------|---------|---------|
| **24.04 LTS → mới nhất** | Có | Có (GNOME ≥45) | Có | Khuyến nghị |
| **22.04 LTS** | Có | Không | Có | GNOME 42 |
| **20.04 LTS** | Có (best-effort) | Không | Không | Setup CLI nếu thiếu GTK4/Adw |

Debian + GNOME: thử nghiệm; nên dùng Ubuntu.

---

## Cài đặt

### Cần gì

- Ubuntu **20.04 trở lên**, phiên GNOME
- Nên chọn **Ubuntu on Xorg** khi đăng nhập (nếu có)
- User thường có `sudo` — **không** chạy AppImage bằng root
- **Theme GDM (màn hình login):** tuỳ chọn, rủi ro cao — mặc định tắt

### Các bước

1. Tải **`Ubuntu-macOS-Theme-Setup-x86_64.AppImage`** từ [Release mới nhất](https://github.com/manguonmocom/ubuntu-macos-theme/releases/latest).
2. Cho phép chạy: chuột phải → **Properties** → **Executable as program**.
3. **Nhấp đúp** AppImage để mở **Setup Wizard** (Ubuntu 20.04 thiếu GTK4/Adw sẽ dùng cài bằng Terminal).
4. Giữ **MacTahoe**. Tuỳ chọn **Ngó Sen**. Nên tắt **GDM** trừ khi bạn hiểu rủi ro.
5. Nhập mật khẩu khi được hỏi. Xong mở **MacTahoe Control** trên Desktop / menu ứng dụng.

```bash
chmod +x Ubuntu-macOS-Theme-Setup-x86_64.AppImage
./Ubuntu-macOS-Theme-Setup-x86_64.AppImage
```

### Sau khi cài

- Một Dock kiểu Mac (Ubuntu 24.04+)
- Theme / icon MacTahoe
- (Tuỳ chọn) Gõ tiếng Việt bằng Ngó Sen — `Ctrl+Space`
- Trên **Wayland**: đăng xuất rồi đăng nhập một lần nếu Dock/Widgets chưa hiện
- Setup luôn ghi **`MacTahoe-Setup-log.txt`** trên Desktop

---

## MacTahoe Control

```bash
mactahoe-control
```

Dòng trạng thái hiện trên và dưới cửa sổ.

### Màu theme

| Mục | Ý nghĩa |
|-----|---------|
| **Accent color** | Default (Tahoe), Blue, Purple, Pink, Red, Orange, Yellow, Green, Grey |
| **Sáng / Tối** | Chế độ Light hoặc Dark |
| **Áp dụng** | Cài biến thể nếu cần, rồi đổi theme + Shell + icon |
| **Theme Select** | Bộ chọn theme GTK4 |

### Dock

| Mục | Ý nghĩa |
|-----|---------|
| **Hiện Dock** | Bật UbuntuTahoeDock |
| **Vị trí Dock** | Trái (kiểu macOS), Dưới, Phải, Trên |
| **Tự ẩn Dock** | Hiện khi đưa chuột vào cạnh màn hình |

### Widgets Desktop

| Mục | Ý nghĩa |
|-----|---------|
| **Hiện Widgets** | Công tắc tổng |
| **Đồng hồ / Thời tiết / Hệ thống / Âm lịch / Nhắc nghỉ** | Từng widget |
| **Cấu hình Widgets nâng cao** | Tuỳ chọn extension |

### Nút cửa sổ

| Mục | Ý nghĩa |
|-----|---------|
| **Vị trí nút** | Trái (macOS ● ● ●) hoặc Phải (Windows/GNOME) |

### Bộ gõ Ngó Sen

Có khi đã cài từ Setup (Ubuntu 22.04+).

| Mục | Ý nghĩa |
|-----|---------|
| **Bật tiếng Việt (Ngó Sen)** | Ưu tiên Ngó Sen; tắt = bàn phím Anh |
| **Sửa bộ gõ Ngó Sen** | Sửa profile fcitx5 và chuyển IM |
| **Cài đặt Ngó Sen / Fcitx5** | Cửa sổ cấu hình |
| **Đặt Ngó Sen làm mặc định** | Profile sạch + `DefaultIM=ngosen` |

**Ctrl+Space** đổi EN ↔ Ngó Sen.

### Công cụ

| Mục | Ý nghĩa |
|-----|---------|
| **Ghi log Control ra Desktop** | **Mặc định tắt.** Bật khi cần gửi `MacTahoe-Control-log.txt`. Log Setup vẫn luôn ghi. |
| **Mở Setup Wizard** | Cài / cập nhật lại |
| **Kích hoạt lại Dock và Widgets** | Nạp lại extension |
| **Quản lý icon / Extension Manager** | Icon và tiện ích GNOME |
| **Áp GTK / Khôi phục kính mờ** | Khôi phục chỉnh GTK và panel |
| **Mở log Setup / Control** | File log trên Desktop |
| **Reset về mặc định Ubuntu** | Trả lại Ubuntu Dock / Yaru |
| **Gỡ MacTahoe** | Gỡ theme/extension (giữ gói Ngó Sen) |

---

## Sự cố nhanh

| Vấn đề | Cách xử lý |
|--------|------------|
| Dock / Widgets chưa hiện | Đăng xuất rồi đăng nhập (nhất là Wayland). Sau đó bật trong Control. |
| Hai Dock | Giữ Dock MacTahoe; tắt Ubuntu Dock. |
| Màn hình “Oh no!” | X11: `Alt+F2` → `r`. Tránh Log Out nếu còn app cần giữ. |
| Không gõ được tiếng Việt | Control → **Sửa bộ gõ Ngó Sen**. |
| Cần chi tiết lúc cài | Desktop: `MacTahoe-Setup-log.txt`. Log Control: bật công tắc trong Công cụ. |
| Ubuntu cũ | 20.04/22.04: theme (và Ngó Sen trên 22.04). Dock/Widgets đủ trên 24.04+. |

**Activities:** phím **Super** (Windows).

---

## English guide

See [GUIDE.md](./GUIDE.md).
