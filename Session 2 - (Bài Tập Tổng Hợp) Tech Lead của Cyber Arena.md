Session 2 - (Bài Tập Tổng Hợp) Tech Lead của Cyber Arena



Phần 1 – Lĩnh vực CNTT và đơn vị lưu trữ\*\*
Chọn ứng viên B. Vì ứng viên B có kĩ thuật lắp ráp, sửa máy tính, cài đặt mạng (về phần cứng) phù hợp với nhu cầu về kĩ thuật mà Teach Lead đang cần. Còn ứng viên A làm về phần mềm chưa phải ưu tiên lúc này.
Sắp xếp theo thứ tự tăng dần: Bit (nhỏ nhất) -> Byte -> KB -> MB -> GB -> TB



Phần 2 – Mô hình IPO và lĩnh vực CNTT
Điền bảng mô hình IPO Hệ thống quay lại và xem lại trận đấu
Thành phần	Trong hệ thống quay/ xem lại trận đấu
Input	Hình ảnh, âm thanh từ trận đấu, các thao tác nút quay video
Process	CPU và Card xử lí đồ họa, mã hóa, nén dữ liệu video
Output	Màn hình hiển thị video và các nền tang phát trực tiếp, phát lại
Storage	Ổ cứng SSD/HDD lưu trữ file video trận đấu
2. Hoạt động của Cyber Arena (livestream, quay video, xem lại phân tích) gắn với lĩnh vực CNTT:
Lĩnh vực 1: Kỹ thuật phần mềm (Software Engineering): Để tổ chức trận đấu cần các phần mềm quay, phát lại trận đấu.
Lĩnh vực 2: Khoa học dữ liệu (Data Science): Thu thập, xử lí, phân tích dữ liệu trận đấu để đưa ra các chỉ số hành động từ đó cho thấy điểm mạnh, điểm yếu các tuyển thủ. Các huấn luyện viên, hỗ trợ sẽ nhìn vào chỉ số này để điều phối đưa ra chiến thuật cho cả đội.



Phần 3 – Tính toán dung lượng và tốc độ mạng

1. Tính dung lượng lưu trữ
20 trận × 500 MB = 10.000 MB
Đổi 10.000 MB = 10.000/1024 ≈ 9,77 GB
SSD 512GB chứa được video của 1 tháng vì video tháng chỉ chiếm khoảng 9,77 GB < 512 GB
->Dung lượng còn trống của ổ trong tháng: 512 - 9,77= 502,23 GB
2. Tính tốc độ mạng:
Đổi 100 Mbps = 100/8 = 12,5 MB/s
Thời gian tối thiểu để tải lên video 200 MB:
t (thời gian) =N (dung lượng)/ v (tốc độ) <=> thời gian = 200/12,5= 16 (s)
Thực tế thường lâu hơn 16 giây là vì suy hao đường truyền, độ trễ mạng, nghẽn mạng cục bộ và máy chủ YouTube, các phần mềm giới hạn tốc độ nhận dữ liệu



Phần 4 - Phần cứng và mô hình DIKW
Lựa chọn: Nâng cấp RAM. Vì khi chơi game nặng kết hợp quay video, phát livestream sẽ tốn rất nhiều bộ nhớ tạm (RAM) nên them RAM để them diện tích chứa dữ liệu tạm giúp máy chạy mượt các tác vụ đa nhiệm hơn mà không bị lag hay tràn bộ nhớ.
2. Bảng mô hình DIKW
BẢNG DI-KW (DATA - INFORMATION - KNOWLEDGE - WISDOM)

|Tầng|Nội dung trong tình huống|Vì sao thuộc tầng này? (1 câu)|
|-|-|-|
|Data (D)|Video trận đấu thô (dữ liệu âm thanh/ hình ảnh được ghi lại)|Là dữ liệu thô chưa qua xử lí gì hết.|
|Information (I)|Tuyển thủ hay bị chết ở phút 15 - 20 trong video|Dữ liệu đã được quan sát, tổng hợp thành thông tin có ý nghĩa.|
|Knowledge (K)|Phát hiện nguyên nhân do thiếu tầm nhìn bản đồ|Rút ra hiểu biết sâu sắc từ việc phân tích thông tin.|
|Wisdom (W)|Yêu cầu mua thêm mắt (Ward) cho trận sau|Ra quyết định sáng suốt để giải quyết vấn đề dựa trên tri thức.|



