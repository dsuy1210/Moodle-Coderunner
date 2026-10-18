# Nhật ký
## Ngày 1 (T1-B1)
- Đã làm: cài Docker, chạy hello-world, cài Git, tạo repo và đẩy lên GitHub
- Lỗi gặp: Docker báo Virtualization not detected (xử lý bằng wsl --install + restart); Git cũ cài ở ổ F đã mất nên phải xoá registry rồi cài lại vào C:\Program Files\Git
- Buổi sau: viết docker-compose cho Jobe + DB

## Ngày 2 (T1-B2)
- Đã làm: viết compose (db + jobe), Jobe chạy được job Python qua REST (outcome 15, stdout 45)
- Cấu hình Jobe: jobe_max_users = 16 (file /var/www/html/jobe/app/Config/Jobe.php dòng 32), nproc = 20
- Lỗi gặp: Docker Desktop chưa chạy nên compose không nối được engine; đường dẫn config Jobe khác dự đoán
- Buổi sau: thêm Moodle vào compose, cài plugin CodeRunner
