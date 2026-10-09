# BitXau Radar - APK Android

Project này đóng gói file `www/index.html` (BitXau Radar) thành app Android. GitHub tự build ra file APK, bạn không cần cài Android Studio.

## Cách làm (làm được hoàn toàn trên điện thoại)
1. Tạo repository mới trên GitHub (ví dụ `bitxau-radar`).
2. Tải toàn bộ nội dung file zip này lên repository (giữ nguyên cấu trúc thư mục, nhớ cả thư mục `.github`).
3. Vào tab **Actions**, chọn workflow **Build APK**, bấm **Run workflow** (hoặc chỉ cần commit là tự chạy). Đợi khoảng 5 đến 8 phút.
4. Tải APK ở một trong hai chỗ:
   - Mục **Releases** của repository (bản `latest`, file `BitXau-Radar.apk`).
   - Hoặc trong lần chạy workflow, mục **Artifacts**.
5. Mở file APK trên điện thoại Android, cho phép "Cài ứng dụng từ nguồn không xác định" nếu máy hỏi.

## Cập nhật app
Thay file `www/index.html` bằng bản mới rồi commit. GitHub sẽ build lại APK và cập nhật vào Releases.

## Lưu ý
- APK này là bản debug, ký bằng khóa debug nên cài được ngay nhưng không đưa lên Google Play được. Nếu cần bản phát hành, hãy tạo keystore riêng và thêm bước ký vào workflow.
- Mỗi lần build có thể ký bằng khóa debug khác nhau, nên khi cài bản mới đè bản cũ Android có thể báo xung đột chữ ký. Khi đó hãy gỡ bản cũ rồi cài lại.
- App cần internet để lấy dữ liệu từ sàn và nguồn lịch kinh tế.
