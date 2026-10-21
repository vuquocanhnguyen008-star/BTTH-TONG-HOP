**Session 3 - (Bài Tập Tổng Hợp) Kiến Trúc Hệ Điều Hành \& Tư Duy Quản Lý File**



**PHẦN 1 — Kiến trúc Hệ điều hành**

1. Chức năng hoạt động là Quản lý bộ nhớ (Memory Management) và Quản lý tiến trình (Process Management). Không bị conflict là vì hệ điều hành sử dung BỘ NHỚ ẢO (Virtual Memory) để cấp phát không gian địa chỉ riêng cho từng phần mềm (World, Chrome, VS Code, Portal). Do đó, các ứng dung hoạt động độc lập mà không xâm phạm vào vùng nhớ của nhau.
2. 
* Khi double click thì shell (giao diện người dung) sẽ ghi nhận thao tác, sau đó chuyển yêu cầu đếnn Kernel (nhân HĐH) để điều khiển phần cứng đọc dữ lieu từ ổ đĩa và tải lên RAM.
* Vai trò của shell: Cầu nối giao tiếp giữa người dung với Kernel, giúp người dung thao tác bằng đồ họa (GUI) hoặc dòng lệnh (CLI) một cách dễ dàng.
* Người dung ít tương tác trực tiếp với Kernel là vì Kernel giao tiếp trực tiếp với phần cứng bằng mã máy/lệnh hệ thống phức tạp, nếu thao tác sai có thể gây hỏng hóc hoặc lỗi hệ thống nghiêm trọng



**Phần 2 - Cây thư mực và ổ đĩa**

1\.

* Xác định Root Dicretory (Thư mục gốc): **D:\\** hoặc **D:**
* Xác định Parent (Thư mục cha) trực tiếp của file anh **1.jpg**: Thư mục **anh. PNG**
* Vai trò của file **anh 1.jpg**: Là "lá" (leaf) trong mô hình cây thư mục (tức là đây là đầu cuối không còn chứa thư mục con nào khác)

2\. 2 lí kỹ thuật:

* Khi tràn ổ đĩa hệ thống (ổ C) chứa HĐH thì sẽ làm bị chậm, đơ hoặc treo
* Mất dữ liệu khi bị lỗi Win. Khi cài lại Win thì toàn bộ dữ liệu ổ C sẽ mất sạch

\-> Đề xuất nơi lưu đúng: Lưu tất cả vào ổ D



**Phần 3: Đường dẫn Path**

1. Ansolute Path (Đường dẫn tuyệt đối) của file: 

**D:\\User\\Desktop\\DonGiaBoThongTin\\BaiTapLop\\Lesson07\\BaoCaoCuoiKy\\SoLieuNguyHiem\\anh\\anh 1.jpg**

2\. Relative Path (Đường dẫn tương đối) chèn **logo.png** vào **report.html**

* Đường dẫn tương đối: **assets/logo.png**
* Lý do: Sử dụng đường dẫn tương đối giúp liên kết vị trí thư mục không bị cố đỉnh ở máy. Khi nén thư mục gửi sang máy khác thì cấu trúc bên trong giữ nguyên không bị gãy (tránh được lỗi "File Not Found")



**Phần 4 - Quy tắc Đặt tên chuẩn**

1\.

Tên chuẩn: **kebab-case: bao-cao-bai-tap-lon-it101-ban-cuoi-v2.docx**



**Phần 5 - Tổ chức và dọn dẹp ổ đĩa**

1\.

* Sổ cấp thư mục đang lồng: Đang lồng 7 cấp thư mục **(User -> Desktop -> DonGiaBoThongTin -> BaiTapLop -> Lesson07 -> BaoCaoCuoiKy -> SoLieuNguyHiem -> anh)**
* Vi phạm quy tắc: 
1. Lồng quá sâu, quá nhiều thư mục (quy tắc 3 cấp thư mục)

2\. Đặt tên (chứa khoảng cách, chữ Tiếng Việt có dấu)

* Thiết kế lại đường dẫn chuẩn: 

**D:\\01\_HocTap\\IT101\_BaiTapLop\\assets\\anh-1.jpg** 

**(Trong đó: Cấp 1 = 01\_HocTap, Cấp 2 = IT101\_BaiTapLop, Cấp 3 = assets)**



**Phần 6 - Đuôi File và File ẩn**

1\.

* Cạm bẫy: Đây là hình thức tấn công bằng mã độc (Phising/Malware) giả dạng file PDF. Dp Window đang ẩn đuôi file mở rộng, file thực tế có dạng **de-thi-dap-an.pdf.exe** hoặc **de-thi-dap-an.pdf.vbs**. Nếu nhấp vào sẽ kích hoạt virus.
* Tên file thật dự đoán: **de-thi-dap-an.pdf.exe**
* Thao tác hiển thị đuôi file trong Windows File Explorer: **Mở File Explorer -> chọn thẻ View trên thanh menu -> tích chọn vào ô File name extensions (Hiện đuôi file)**

