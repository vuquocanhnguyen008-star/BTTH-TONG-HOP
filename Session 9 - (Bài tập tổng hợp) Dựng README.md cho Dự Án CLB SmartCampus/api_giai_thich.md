# Hướng Dẫn Giải Thích Thuật Ngữ API
## Nội Dung Yêu Cầu Gửi AI

### Thông Tin Nền Tảng
- **Vai trò**: Thành viên mới của Câu lạc bộ Lập trình PTIT, tham gia phát triển dự án SmartCampus (ứng dụng tra cứu lịch học, phòng trống và thông báo).
- **Vấn đề**: Chưa nắm rõ khái niệm API.

### Mục Tiêu Xử Lý
- Làm rõ khái niệm API (Application Programming Interface) theo hướng trực quan, dễ tiếp cận cho người mới bắt đầu.
- Lấy ví dụ thực tế gắn liền với tính năng tra cứu lịch học của SmartCampus.
- Tóm tắt gọn gàng cách thức ứng dụng và máy chủ truyền nhận thông tin qua lại.
- Kết luận bằng một câu đúc kết ngắn gọn, dễ nhớ.

### Phạm Vi Cần Tránh
- Không đi sâu vào cấu trúc giao thức, các biện pháp bảo mật, mã nguồn cụ thể hay phân loại các dạng API phức tạp.

## Nội Dung Phản Hồi Từ AI

### Khái Niệm API Là Gì?
**API** (Giao diện lập trình ứng dụng - Application Programming Interface) được xem như bộ quy chuẩn cho phép các phần mềm giao tiếp và trao đổi thông tin với nhau. Có thể ví API như một nhân viên phục vụ nhận món: ứng dụng truyền đi yêu cầu theo đúng định dạng, máy chủ tiếp nhận, xử lý rồi gửi lại kết quả tương ứng.

### Minh Hoạ Qua Ứng Dụng SmartCampus
Khi một sinh viên điền mã số sinh viên để tra cứu lịch học, ứng dụng sẽ truyền mã này đến máy chủ thông thông qua API. Máy chủ tiến hành tra cứu dữ liệu phù hợp và phản hồi lại kết quả lịch học; từ đó ứng dụng hiển thị chính xác các môn học và khung thời gian cho người dùng.

### Tổng Kết Nhanh
API đóng vai trò là giao ước giúp các phần mềm tương tác nhịp nhàng. Ứng dụng đưa ra yêu cầu, máy chủ xử lý và trả về thông tin. Tóm lại, API giống như một chiếc cầu nối trung gian giúp phần mềm truy xuất dữ liệu từ hệ thống khác.

### Đúc Kết Sau 3 Bước Đọc
API là chuẩn mực kết nối phần mềm để truyền tải dữ liệu. Trong SmartCampus, ứng dụng gửi mã sinh viên lên máy chủ nhờ API để lấy lịch học và nhận lại thông tin hiển thị. Nhìn chung, API hoạt động như nhịp cầu nối liền ứng dụng và hệ thống máy chủ.

## Các Bước Thực Hiện Lưu Trữ Tài Liệu Markdown
1. Soạn thảo prompt bao gồm bối cảnh, nội dung mục tiêu và các tiêu chí rõ ràng.
2. Chuyển prompt sang AI để lấy câu trả lời phù hợp.
3. Đọc hiểu nội dung theo trình tự: tiêu đề, từ khóa in đậm, các ý chính; sau đó tự viết lại bản tóm tắt bằng văn phong cá nhân.
4. Đưa prompt, phần đáp án và tóm tắt vào ứng dụng StackEdit, lưu trữ hoặc tải về dưới định dạng `api_giai_thich.md`.