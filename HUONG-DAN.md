# Theme macOS cho Ubuntu — Hướng dẫn (Tiếng Việt)

Cài **giao diện giống macOS trên Ubuntu** (MacTahoe): theme, Dock, Widgets, và tuỳ chọn bộ gõ **Ngó Sen**.

Từ khóa: *theme macOS Ubuntu* · *làm Ubuntu giống Mac* · *MacTahoe* · *Dock GNOME* · *Ubuntu 24.04 theme*.

---

## Cài đặt

### Cần gì

- Ubuntu **24.04** (tốt nhất). 22.04: theme / Ngó Sen; Dock + Widgets cần GNOME ≥ 45. **20.04: không hỗ trợ.**
- Nên dùng phiên **Ubuntu on Xorg**.
- User thường có `sudo` — **không** chạy installer bằng `sudo`.
- **Theme GDM (màn hình login):** tuỳ chọn. Shell **46** (24.04) dùng đường classic; Shell **48+** đường mới; Shell **42** (22.04) thử nghiệm. Nên **tắt** trừ khi chấp nhận rủi ro login.

### Các bước (ứng dụng đồ họa)

1. Tải **`Ubuntu-macOS-Theme-Setup-x86_64.AppImage`** từ [Release mới nhất](https://github.com/manguonmocom/ubuntu-macos-theme/releases/latest).
2. Cho phép chạy: chuột phải → **Properties** → bật **Executable as program** (hoặc Allow Launching).
3. **Nhấp đúp** file AppImage — cửa sổ **Setup Wizard** mở ra, không cần Terminal.
4. Trong Wizard:
   - Giữ **MacTahoe** (theme + Dock + Widgets).
   - Bật **Ngó Sen** nếu cần gõ tiếng Việt.
   - Nên tắt **theme GDM** trừ khi bạn hiểu rủi ro.
5. Nhập mật khẩu khi được hỏi. Xong mở **MacTahoe Control** trên Desktop / menu ứng dụng.

Tuỳ chọn (terminal):

```bash
chmod +x Ubuntu-macOS-Theme-Setup-x86_64.AppImage
./Ubuntu-macOS-Theme-Setup-x86_64.AppImage
```

### Kiểm tra nhanh

- Chỉ **một** Dock kiểu Mac (không hai Dock).
- Theme / icon MacTahoe.
- (Tuỳ chọn) Gõ tiếng Việt bằng Ngó Sen — `Ctrl+Space` đổi bàn phím.

Dock/Widgets chưa hiện lần đầu: đăng xuất rồi đăng nhập lại.

---

## Dùng MacTahoe Control

Mở **MacTahoe Control** từ menu, Desktop, hoặc:

```bash
mactahoe-control
```

Dòng trạng thái hiện **trên và dưới** cửa sổ sau mỗi thao tác.

### Màu theme (Color Themes)

Chọn **màu nhấn** và sáng/tối kiểu MacTahoe.

| Mục | Ý nghĩa |
|-----|---------|
| **Accent color** | Màu nhấn: Default (Tahoe), Blue, Purple, Pink, Red, Orange, Yellow, Green, Grey. |
| **Sáng / Tối** | Chế độ Light hoặc Dark cho GTK + Shell. |
| **Áp dụng** | Cài biến thể nếu thiếu, rồi đổi theme, Shell và icon cùng lúc. |
| **Theme Select → Mở** | Mở bộ chọn theme GTK4 (`gnome-theme-switcher`) để chọn nâng cao. |

Gợi ý: sau Áp dụng, mở lại Quick Settings. X11: `Alt+F2` → `r` nếu Shell chưa đổi.

### Dock

Thanh ứng dụng kiểu Mac (UbuntuTahoeDock). Ubuntu Dock mặc định được tắt để tránh hai Dock.

| Mục | Ý nghĩa |
|-----|---------|
| **Hiện Dock** | Bật / tắt extension Dock MacTahoe. |
| **Vị trí Dock** | Trái (giống macOS), Dưới, Phải, hoặc Trên. |
| **Tự ẩn Dock** | Ẩn Dock đến khi đưa chuột vào cạnh màn hình. |

### Widgets Desktop

Widget trên nền desktop (UbuntuTahoeWidgets).

| Mục | Ý nghĩa |
|-----|---------|
| **Hiện Widgets** | Công tắc tổng cho cả bộ widget. |
| **Đồng hồ lớn** | Đồng hồ lớn trên desktop. |
| **Thời tiết** | Widget thời tiết. |
| **Giám sát hệ thống** | CPU / bộ nhớ kiểu theo dõi hệ thống. |
| **Âm lịch** | Widget âm lịch. |
| **Nhắc nghỉ** | Nhắc nghỉ giải lao. |
| **Mở cấu hình Widgets nâng cao** | Mở cửa sổ tuỳ chọn extension. |

### Nút cửa sổ

Vị trí nút đóng / thu nhỏ / phóng to trên thanh tiêu đề.

| Mục | Ý nghĩa |
|-----|---------|
| **Vị trí nút** | **Trái — kiểu macOS (● ● ●)** hoặc **Phải — Windows/GNOME**. |

### Bộ gõ tiếng Việt (Ngó Sen)

IME fcitx5 (nếu đã cài Ngó Sen trong Setup).

| Mục | Ý nghĩa |
|-----|---------|
| **Bật tiếng Việt (Ngó Sen)** | Chuyển sang Ngó Sen và ưu tiên làm bộ gõ mặc định. Tắt = bàn phím Anh (US). |
| **Sửa bộ gõ Ngó Sen** | Ghi lại profile/config fcitx5 và khởi động lại khi không gõ được hoặc hay nhảy về EN. |
| **Cài đặt Ngó Sen → Mở** | Cửa sổ cấu hình chính thức của Ngó Sen. |
| **Cấu hình Fcitx5 → Mở** | Thêm/bớt bộ gõ, phím tắt. |
| **Đặt Ngó Sen làm mặc định** | Giống Sửa: profile sạch + `DefaultIM=ngosen`. |

Gợi ý: **Ctrl+Space** đổi EN ↔ Ngó Sen. Hay về EN khi đổi app: bấm **Sửa** một lần.

### Công cụ

Bảo trì desktop MacTahoe.

| Mục | Ý nghĩa |
|-----|---------|
| **Mở Setup Wizard** | Chạy Setup lại để cập nhật / cài lại. |
| **Kích hoạt lại Dock và Widgets** | Nạp lại Dock/Widgets nếu bị mất (thường không cần logout). |
| **Quản lý icon / Extension Manager** | Quản lý icon MacTahoe hoặc extension GNOME (khi đã cài). |
| **Áp dụng lại GTK overrides** | Khôi phục chỉnh GTK của Setup (ví dụ thanh đường dẫn Files). |
| **Khôi phục kính mờ MacTahoe** | Khôi phục Quick Settings / panel kiểu kính. |
| **Reset về mặc định Ubuntu** | Gỡ look Mac, bật lại Ubuntu Dock / Yaru. Shortcut Setup vẫn giữ để cài lại. |
| **Gỡ MacTahoe** | Gỡ theme/extension MacTahoe. Gói Ngó Sen giữ nguyên trừ khi gỡ riêng. Shortcut Setup được khôi phục. |

---

## Sự cố nhanh

| Vấn đề | Cách xử lý |
|--------|------------|
| Màn hình “Oh no!” | **Đừng Log Out** nếu còn app cần giữ. X11: `Alt+F2` → `r`. |
| Hai Dock | Trong Control giữ Dock MacTahoe; Ubuntu Dock phải tắt. |
| Ngó Sen → English | Control → **Sửa bộ gõ Ngó Sen**. |
| File log | `~/.local/state/mactahoe-ubuntu/shell.log` |

**Activities:** phím **Super** (Windows). Menu Apple chỉ hiện hướng dẫn.

---

## English guide

See [GUIDE.md](./GUIDE.md).
