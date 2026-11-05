# 1. Phân tích rủi ro của kỹ thuật "Đuôi file kép" (Double Extension)

## Cơ chế

Hacker đặt tên tệp dạng `HoaDon_T10.pdf.exe`. Mặc định Windows **ẩn phần mở rộng của các loại tệp đã biết**, nên người dùng chỉ thấy `HoaDon_T10.pdf`, kèm biểu tượng giả giống file PDF/Word. Người dùng tưởng là tài liệu nên bấm mở, trong khi thực chất đang chạy một tệp thực thi (`.exe`, `.scr`, `.bat`, `.js`...).

## Rủi ro

- Mã độc tự động kết nối về máy chủ của hacker, đánh cắp mật khẩu, tài khoản mạng xã hội, ngân hàng và thông tin lưu trong trình duyệt.
- Hacker có thể điều khiển từ xa: di chuột, chụp màn hình, ghi phím gõ (keylogger).
- Tải thêm mã độc khác (ransomware mã hóa dữ liệu, trojan, botnet) và chạy các dòng lệnh ẩn.
- Lây lan sang hệ thống khác (gửi email giả mạo từ tài khoản nạn nhân, lây qua mạng nội bộ), gây thiệt hại cho cả tổ chức.

### Vì sao kỹ thuật này hiệu quả

Nó đánh vào yếu tố con người (tin tưởng tệp "tài liệu công việc") và thường đi kèm nội dung email gấp gáp, giả danh đối tác hoặc cấp trên.

---

# 2. Vì sao yêu cầu "Tắt Antivirus" là cái bẫy

- Antivirus là lớp phòng thủ giúp phát hiện và chặn mã độc. Khi bị tắt, mã độc chạy mà không bị cản trở.
- Một tệp **hợp pháp** không bao giờ cần bạn tắt phần mềm bảo mật. Hacker yêu cầu vì **tệp đó đã bị Antivirus nhận diện là độc hại**, hoặc họ biết nó sẽ bị chặn.
- Đây là chiêu **thao túng tâm lý (social engineering)**: viện cớ "phần mềm báo nhầm", "file được mã hóa nên bị chặn" để dụ nạn nhân tự gỡ bỏ hàng rào bảo vệ.
- Hậu quả: máy bị chiếm quyền, mất tài khoản, mất dữ liệu và có thể bị tống tiền.

**Kết luận:** Bất kỳ email hay phần mềm nào yêu cầu tắt Antivirus/Firewall đều phải coi là **dấu hiệu lừa đảo** và không được làm theo.

---

# 3. Công cụ quét tệp trực tuyến trước khi mở

## VirusTotal (virustotal.com)

Tải tệp (hoặc dán đường link/hash) lên để được quét bởi hơn 70 engine Antivirus cùng lúc. Kết quả cho biết bao nhiêu engine phát hiện mã độc.

## Lưu ý khi dùng

- Không tải lên tệp chứa thông tin nhạy cảm, vì tệp upload có thể được chia sẻ với cộng đồng bảo mật.
- Kết quả "sạch" **không đảm bảo 100% an toàn** (mã độc mới có thể chưa bị nhận diện). Nếu email vẫn đáng ngờ, hãy tránh mở.
- Có thể dùng thêm **Hybrid Analysis** hoặc **Any.run** (môi trường sandbox) để xem hành vi thực tế của tệp.

---

# 4. Biện pháp bổ sung

- Bật hiển thị phần mở rộng tệp trong Windows: *File Explorer → View → File name extensions*.
- Xác minh người gửi qua kênh khác (gọi điện, nhắn tin).
- Không mở tệp từ email lạ; báo cáo cho bộ phận IT/an ninh mạng.
- Nếu đã lỡ mở: ngắt mạng ngay, quét toàn bộ máy, đổi mật khẩu từ thiết bị sạch, báo IT.
