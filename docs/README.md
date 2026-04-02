🚀 Transport Booking System - Search Module
Dự án này là hệ thống đặt vé máy bay và tàu hỏa trực tuyến. Tôi chịu trách nhiệm chính cho Module Search (Tìm kiếm & Tra cứu) — đây là "cửa ngõ" quan trọng nhất, nơi bắt đầu hành trình trải nghiệm của khách hàng.

👤 Thông tin thành viên
Họ tên: Phong

Vai trò: Backend & Frontend Developer (Search Module)

Phạm vi phụ trách: Xây dựng luồng tìm kiếm chuyến bay/tàu, bộ lọc nâng cao, trang chi tiết chuyến đi và tích hợp kiểm tra tình trạng chỗ trống.

🛠 Công nghệ sử dụng (Gợi ý)
Frontend: Next.js / React, Tailwind CSS.

Backend: Node.js, Express.js.

Database: MongoDB (Mongoose).

API: RESTful API.

📖 Mô tả chi tiết chức năng
1. Tìm kiếm Chuyến bay & Chuyến tàu
Hỗ trợ người dùng tra cứu chuyến đi dựa trên các tham số linh hoạt.

Dữ liệu đầu vào: Điểm đi, điểm đến, ngày khởi hành, số lượng hành khách.

Xử lý logic: * Kiểm tra tính hợp lệ (ví dụ: ngày khởi hành không được ở quá khứ, điểm đi và đến không được trùng nhau).

Truy vấn Database động dựa trên phương tiện (Flight/Train).

Trả về thông tin: Mã chuyến, hãng vận chuyển, lịch trình và giá vé cơ bản.

2. Bộ lọc kết quả nâng cao (Filtering)
Tối ưu hóa trải nghiệm tìm kiếm giúp người dùng tìm được chuyến đi phù hợp nhất.

Tiêu chí lọc: Giá vé (tăng/giảm), khung giờ khởi hành, hãng vận chuyển, hạng ghế.

Cơ chế xử lý: Thực hiện lọc trực tiếp thông qua Database Query để đảm bảo tốc độ và độ chính xác của dữ liệu.

3. Xem chi tiết & Kiểm tra chỗ khả dụng
Bước đệm quan trọng trước khi chuyển sang sơ đồ chọn ghế (Seat Map).

Thông tin chi tiết: Hiển thị toàn bộ thông số chuyến đi và số lượng ghế còn trống ước tính.

Lưu ý: Chức năng này lấy dữ liệu tổng quát (Available/Full), logic chọn ghế realtime sẽ được xử lý ở module tiếp theo.

🔄 Luồng xử lý (Search Flow)
Quy trình:

Trang chủ: User nhập thông tin tìm kiếm.

Kết quả: Hiển thị danh sách (Flight/Train) -> Áp dụng bộ lọc (Filter).

Chi tiết: User chọn chuyến -> Xem chi tiết & Trạng thái ghế.

Chuyển giao: Kết thúc luồng Search và chuyển sang bước chọn ghế (Module Seat).

🎨 Giao diện thực hiện
Tôi đã thiết kế và triển khai 6 giao diện chính đảm bảo tính Responsive và thân thiện với người dùng:

Trang Đăng ký/Đăng nhập: Validation trực tiếp, giao diện tối giản.

Trang Kết quả (Flight/Train): Bố cục dạng danh sách chuyên nghiệp, tích hợp Sidebar lọc.

Trang Chi tiết chuyến đi: Tập trung vào thông tin quan trọng nhất và nút hành động (Call to action).

Trang Thanh toán thất bại: Thông báo lỗi trực quan và điều hướng hỗ trợ người dùng thử lại.


📟 Tài liệu API (API Endpoints)
GET,/search/flights,Tìm kiếm chuyến bay theo params

GET,/search/trains,Tìm kiếm chuyến tàu theo params

GET,/search/filter,Lấy dữ liệu danh sách đã qua bộ lọc

GET,/trips/:id,Lấy thông tin chi tiết của một chuyến đi

GET,/trips/:id/availability,Kiểm tra tình trạng ghế trống
