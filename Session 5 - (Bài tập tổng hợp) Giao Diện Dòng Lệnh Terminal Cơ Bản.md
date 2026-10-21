# Session 5 - (Bài tập tổng hợp) Giao Diện Dòng Lệnh Terminal Cơ Bản

## Phần 1: CLI vs GUI và Cấu Trúc Câu Lệnh

### 1\. Phân tích thành phần câu lệnh PowerShell

Xét câu lệnh mẫu: `ls -Force C:\\Windows\\Logs`

* **Command:** `ls`
* **Options/Flags:** `-Force`S
* **Argument:** `C:\\Windows\\Logs`

### 2\. Lý do nhóm bắt buộc phải dùng Terminal (PowerShell/SSH) cho máy chủ Cloud

* Máy chủ Cloud thường hoạt động ở dạng **headless** (không có giao diện đồ họa).
* Việc chạy desktop trên server tiêu tốn rất nhiều RAM và CPU trong khi người dùng phải chi trả chi phí theo cấu hình phần cứng.
* Nhà cung cấp chỉ thiết lập dòng lệnh, đòi hỏi nhóm phải kết nối từ xa thông qua giao thức SSH.
* Kênh kết nối này chỉ truyền tải văn bản, không hỗ trợ cửa sổ hay chuột, do đó gõ lệnh là phương thức duy nhất để tạo thư mục, sao chép project hoặc thực thi chương trình trên server.

## Phần 2: Điều Hướng Hệ Thống File

1. **Relative Path di chuyển vào thư mục dự án:**

   * Từ vị trí hiện tại tại `C:\\Users\\student\\Desktop`, sau khi thư mục `quan-ly-sinh-vien` được tạo, lệnh sử dụng là: `cd .\\quan-ly-sinh-vien`.
2. **Absolute Path chuẩn Windows tới file `main.py`:**

   * Đường dẫn đầy đủ: `C:\\Users\\student\\Desktop\\quan-ly-sinh-vien\\src\\main.py`.
3. **Lệnh xem toàn bộ nội dung thư mục đồng cấp `data\\` (kể cả file ẩn) khi đang đứng ở `src\\`:**

   * Lệnh PowerShell duy nhất: `ls -Force ..\\data`.

## Phần 3: Thao Tác File và Thư Mục

* **Tạo đồng thời hai thư mục con `src` và `data` bên trong `quan-ly-sinh-vien`:**
`mkdir quan-ly-sinh-vien\\src, quan-ly-sinh-vien\\data`
* **Tạo ba file rỗng (`main.py`, `utils.py`, `README.md`) trong một dòng lệnh duy nhất:**
`New-Item src\\main.py, src\\utils.py, README.md -ItemType File`
* **Đổi tên và sao lưu thư mục dự án:**

  * Đổi tên thư mục gốc từ `quan-ly-sv` thành `quan-ly-sinh-vien`: `mv quan-ly-sv quan-ly-sinh-vien`.
  * Sao lưu toàn bộ thư mục kèm theo các nội dung con bằng cờ đệ quy: `cp quan-ly-sinh-vien backup-quan-ly-sinh-vien -Recurse`.

## Phần 4: Xử Lý Lỗi Terminal

### 1\. Chẩn đoán Log lỗi số 2 (mục 3d)

* **Nguyên nhân:** Lỗi gõ sai tên lệnh `cd scr` (thiếu chữ `r` ở đúng vị trí), trong khi tên thư mục chính xác là `src` khiến PowerShell báo không tìm thấy đường dẫn.
* **Cách kiểm tra bằng phím Tab:** Gõ `cd s` rồi nhấn phím `Tab` để PowerShell tự động điền tên thư mục bắt đầu bằng chữ `s` tại vị trí hiện tại. Nếu hệ thống tự điền ra `src`, tức là thư mục tồn tại và lỗi xuất phát từ việc gõ sai. Nếu phím Tab không điền gì, thư mục không tồn tại ở đó, lúc này cần gõ `ls` để xem danh sách thực tế và kiểm tra lại vị trí đang đứng.

### 2\. Chẩn đoán và khắc phục Log lỗi số 3 (mục 3e)

* **Nguyên nhân:** Thông báo `Access is denied` cho thấy hệ thống thiếu quyền thực thi; trên Windows, tài khoản thông thường không đủ đặc quyền để chạy các thao tác mà script cài đặt yêu cầu.
* **Cách khắc phục:** Đóng cửa sổ hiện tại, gõ từ khóa `PowerShell` vào thanh tìm kiếm của Windows, nhấn tổ hợp phím `Ctrl + Shift + Enter` để mở bằng quyền **Administrator**, sau đó di chuyển (`cd`) trở lại thư mục chứa script và chạy lại lệnh `.\\setup.ps1`.

### 3\. Xử lý cảnh báo Log lỗi số 1 (mục 3c)

* **Nguyên nhân:** PowerShell đưa ra cảnh báo vì thư mục `old-version` có chứa file bên trong, nhưng lệnh `rm` không được đính kèm cờ `-Recurse` nên hệ thống không xác định được người dùng có muốn xóa luôn phần nội dung bên trong hay không. Cảnh báo này giúp tránh xóa nhầm vì dữ liệu bị xóa bằng lệnh này không đi qua thùng rác và không thể khôi phục.
* **Lệnh xóa thành công không bị hỏi xác nhận:** `rm old-version -Recurse -Force`.

### 4\. Phân tích Log lỗi số 4 (mục 3f) theo Quy trình 3 bước

* **(a) Dòng chứa thông điệp lỗi trực tiếp nhất:** `FileNotFoundError: \[Errno 2] No such file or directory: 'data/input.csv'`.
* **(b) Từ khóa lỗi (Error Keyword):** `FileNotFoundError` và `No such file or directory`.
* **(c) Điều cần kiểm tra tiếp để sửa lỗi:** Vị trí hiện tại đang đứng là `...\\quan-ly-sinh-vien\\src`, trong khi đoạn code mở file `data/input.csv` bằng Relative Path tính từ thư mục thực thi lệnh. Python tìm kiếm tại `src\\data\\input.csv` nên không tìm thấy, trong khi đường dẫn thực tế của file nằm ở `quan-ly-sinh-vien\\data\\input.csv`.

