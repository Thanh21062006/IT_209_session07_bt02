# Bài 2: Quản trị Tường lửa UFW cho Cụm Dịch vụ Multi-port

## 1. Các lệnh cấu hình UFW đã thực hiện

```bash
# Khai báo các chính sách mặc định
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Cho phép các cổng dịch vụ quy định
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 8082/tcp

# Kích hoạt UFW
sudo ufw enable
```

## 2. Trạng thái ufw chi tiết

Kết quả đầu ra của lệnh `sudo ufw status verbose`:

```text
Status: active
Logging: on (low)
Default: deny (incoming), allow (outgoing), disabled (routed)
New profiles: skip

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW IN    Anywhere
80/tcp                     ALLOW IN    Anywhere
8082/tcp                   ALLOW IN    Anywhere
22/tcp (v6)                ALLOW IN    Anywhere (v6)
80/tcp (v6)                ALLOW IN    Anywhere (v6)
8082/tcp (v6)              ALLOW IN    Anywhere (v6)
```
*(Có thể thay thế bằng ảnh chụp màn hình terminal thực tế)*
