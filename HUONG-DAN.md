# SCAN DOC V1.5 – Hướng dẫn cài đặt

App là một PWA thuần (HTML + JS), **không cần server xử lý**, mọi ảnh được xử lý ngay trên điện thoại.

## Các file

| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ app (giao diện + nhận diện giấy + chỉnh phối cảnh + bộ lọc + tạo PDF) |
| `manifest.webmanifest` | Thông tin để "Cài đặt app" lên màn hình chính |
| `sw.js` | Service worker – cho app mở được khi không có mạng |
| `icon-*.png` | Biểu tượng app |

## Đưa app lên mạng (bắt buộc HTTPS để dùng camera)

**Cách nhanh nhất – Netlify Drop (miễn phí, 1 phút):**
1. Trên máy tính, mở https://app.netlify.com/drop
2. Giải nén file zip, kéo **cả thư mục `scandoc`** thả vào trang.
3. Netlify cho bạn một link dạng `https://xxx.netlify.app` → mở link đó bằng Chrome trên điện thoại.

**Hoặc GitHub Pages:** tạo repo, upload 6 file, vào Settings → Pages → chọn nhánh `main` → dùng link `https://<tên>.github.io/<repo>/`.

## Cài lên điện thoại Android
1. Mở link bằng **Chrome**.
2. Menu ⋮ → **Cài đặt ứng dụng** (hoặc "Thêm vào màn hình chính").
3. Lần đầu bấm CHỤP TÀI LIỆU, chọn **Cho phép** dùng camera.

## Lưu ý
- PDF và ảnh JPG lưu vào thư mục **Download** của máy.
- Nút **CHIA SẺ** mở bảng chia sẻ của Android (Zalo, Messenger, Gmail, Drive…).
- Tài liệu đã tạo được giữ trong app (mục TÀI LIỆU ĐÃ LƯU). Xóa dữ liệu Chrome sẽ xóa luôn các tài liệu này.
- Trang đang chụp dở được tự lưu; nếu app bị tắt giữa chừng, mở lại sẽ thấy nút **Tiếp tục**.
- AUTO: khi nhận diện được giấy và bạn giữ yên máy ~1,3 giây, app tự chụp. Tắt AUTO để chỉ chụp bằng nút.
- A4 và A5 có cùng tỉ lệ (≈ 1 : 1,414) nên ảnh cắt giống nhau; PDF luôn là khổ A4, trang ngang tự xoay ngang.
