# Sổ Tiền — demo

Web app quản lý tiền: quét VietQR → nhập số tiền → mở app ngân hàng để chuyển. Ghi lại tiền vào/ra từ SMS, email, thông báo.

## Tính năng
- Quét mã VietQR (camera hoặc ảnh) → tự điền ngân hàng, số tài khoản, số tiền, nội dung
- Nhập tay khi không có QR, danh bạ người nhận
- Mở app ngân hàng qua deeplink VietQR (MB Bank tự điền; ngân hàng khác dùng ảnh QR)
- Đọc SMS / email / thông báo (dán vào) → tự nhận tiền vào/ra, số dư
- Tự khớp lệnh chuyển với tin báo biến động, chống trùng giao dịch
- Đối soát số dư, lịch sử, thống kê 7 ngày

## Chạy trên GitHub Pages
1. Tạo repo mới, upload `index.html` và `README.md`
2. Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save
3. Sau 1–2 phút, mở `https://<username>.github.io/<tên-repo>/`

Chạy trên máy: mở `index.html` bằng trình duyệt (camera chỉ hoạt động qua HTTPS hoặc localhost).

## Lưu ý
- Dữ liệu lưu trong trình duyệt (localStorage), chưa có Supabase
- Đọc thông báo/SMS tự động cần app native (Android) hoặc Phím tắt iOS — bản web mô phỏng bằng cách dán nội dung
- Deeplink tự điền phụ thuộc từng ngân hàng (theo danh sách của VietQR.io)
- Mã BIN của Timo và một số ngân hàng nhỏ cần kiểm tra lại
- Bản demo, chưa dùng cho giao dịch thật ở quy mô lớn
