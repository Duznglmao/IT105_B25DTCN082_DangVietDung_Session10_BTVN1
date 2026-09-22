# THỰC HÀNH VẼ BIỂU ĐỒ TUẦN TỰ CHỨC NĂNG ĐĂNG NHẬP RIKKEISHOP
## Bước 1: Đọc kịch bản nghiệp vụ
Trước khi bắt đầu vẽ biểu đồ tuần tự thì ta sẽ phân tích qua:

Đầu tiên, bài có 3 đối tượng gồm khách hàng, màn hình UI, AuthServer

Tiếp theo, khách hàng gửi nhapThongTin(username, password) cho màn hình UI. Đây là thông điệp đồng bộ

UI gửi verifyAccount() cho AuthServer và chờ kết quả nên đây là thông điệp đồng bộ

AuthServer tự gọi checkCredentials() nên đây là self-message

Sau khi kiểm tra, dùng alt với hai điền kiện [Thông tin hợp lệ] và [Thông tin không hợp lệ]

Nếu hợp lệ: AuthServer trả Token cho UI, UI trả phản hồi hiển thị trang chủ cho Khách hàng

còn không thì AuthServer trả lỗi cho UI, UI trả phản hồi hiển thị cảnh báo lỗi cho Khách hàng

## Bước 2: Vẽ
