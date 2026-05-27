# AIBIZ Landing Page

Bộ file website tĩnh cho aibiz.com.vn.

## Cấu trúc
- index.html
- assets/logo-aibiz.png
- assets/ngo-phu-manh-placeholder.svg

## Lưu ý
Ảnh chuyên gia hiện là placeholder. Khi có ảnh thật, đổi tên ảnh thành `ngo-phu-manh.png`, đưa vào thư mục `assets` và sửa trong `index.html`:
`assets/ngo-phu-manh-placeholder.svg` thành `assets/ngo-phu-manh.png`.

## Deploy GitHub Pages
Upload `index.html` và thư mục `assets` lên repository. Bật Settings → Pages → Deploy from branch → main/root.

## Kết nối form với Google Sheet

Form trong `index.html` đã được chuyển sang gửi dữ liệu qua Google Apps Script Web App. Làm theo các bước sau:

1. Tạo một Google Sheet mới bằng tài khoản muốn nhận lead.
2. Trong Google Sheet, chọn Extensions → Apps Script.
3. Xóa nội dung mặc định, dán toàn bộ mã trong file `google-apps-script.gs`.
4. Bấm Save.
5. Bấm Deploy → New deployment.
6. Chọn type là Web app.
7. Execute as: Me.
8. Who has access: Anyone.
9. Bấm Deploy, cấp quyền truy cập cho script.
10. Copy Web app URL.
11. Mở `index.html`, tìm dòng:
   `const GOOGLE_SCRIPT_URL = '';`
12. Dán URL vào giữa dấu nháy:
   `const GOOGLE_SCRIPT_URL = 'https://script.google.com/macros/s/.../exec';`

Sau khi kết nối, mỗi lượt đăng ký sẽ được ghi vào sheet `AIBIZ Leads` và gửi email thông báo về `phumanhai@gmail.com`.
