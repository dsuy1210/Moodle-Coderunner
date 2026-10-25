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

## Ngày 3-4 (T1-B3, T1-B4)
- Đã làm: thêm Moodle vào compose, cài 2 plugin CodeRunner, tạo course PY01, 10 user, câu sum_even, quiz adaptive
- Lỗi 1: Moodle không gọi được Jobe, "Failed to run tests". Nguyên nhân: Moodle chặn cURL tới dải mạng riêng 172.16.0.0/12 (mạng Docker). Cách sửa: bỏ dòng này khỏi cURL blocked hosts list (Site administration > General > Security > HTTP security)
- Lỗi 2: chạy purge_caches.php bằng CLI làm Moodle báo "File store path does not exist", phải dựng lại (docker compose down -v). Bài học: xoá cache bằng giao diện
- Lỗi 3: IndentationError do dán code có khoảng trắng đầu dòng
- Buổi sau: ca lỗi và giới hạn tài nguyên (tuần 2)

## Ngày 5 (T2-B1)
- Đã làm: 3 câu hàm (sum_even, reverse_string, count_words), mỗi câu có test thường, biên, ẩn
- Ca sai thử: (ghi thông báo bạn thấy ở khối 3)
- Lỗi gặp:
- Buổi sau: câu đọc stdin, so sánh template combinator và per-test
