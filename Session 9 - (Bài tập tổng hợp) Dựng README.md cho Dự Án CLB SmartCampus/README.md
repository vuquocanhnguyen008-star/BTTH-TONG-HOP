# Ứng Dụng SmartCampus 🎓
**SmartCampus** là nền tảng di động thiết kế riêng cho sinh viên PTIT nhằm hỗ trợ tra cứu *thời khóa biểu*, tìm kiếm phòng học trống cũng như tiếp nhận các thông báo mới nhất từ phía nhà trường.

## Các Tính Năng Nổi Bật
- Tra cứu nhanh lịch học dựa vào mã định danh sinh viên.
  - Trích xuất chi tiết thời khóa biểu tương ứng với mã sinh viên nhập vào.
- Tra cứu danh sách các phòng học còn trống phân bổ theo từng tòa nhà.

[Trang Chủ CLB Lập Trình PTIT](https://clblaptrinh.ptit.edu.vn)

![Logo SmartCampus](https://placehold.co/256x256?text=SmartCampus)

> ⚠️ Lưu ý: Dự án hiện vẫn trong quá trình phát triển và chưa được đưa vào vận hành chính thức.

## Hướng Dẫn Cài Đặt Hệ Thống
git clone [https://github.com/clb-lap-trinh/smartcampus.git](https://github.com/clb-lap-trinh/smartcampus.git)
npm install
npm start

## Tiến Trình Xây Dựng Tính Năng

* [x] Tính năng tra cứu lịch học theo mã sinh viên
* [x] Tính năng xem phòng học trống theo khu vực tòa nhà
* [ ] Tích hợp thông báo đẩy (push notification)
* [ ] Đăng nhập hệ thống bằng tài khoản sinh viên trường cấp

## Các Thư Viện Sử Dụng

| Thư Viện | Phiên Bản | Vai Trò |
| --- | --- | --- |
| React Native | 0.74 | Xây dựng giao diện đa nền tảng cho cả iOS và Android |
| Axios | 1.6 | Hỗ trợ thực hiện gọi API để truy xuất dữ liệu lịch học |

## 🚀 Tài Liệu API Liên Quan

Khái niệm API được ứng dụng để lấy dữ liệu lịch học của hệ thống. Bạn có thể xem bản giải thích chi tiết tại tệp [`api_giai_thich.md`](https://www.google.com/search?q=api_giai_thich.md).

*Mẹo định dạng Markdown:* Dùng cú pháp `\*` để hiển thị nguyên bản dấu sao thay vì dùng nó làm ký hiệu định dạng văn bản.
