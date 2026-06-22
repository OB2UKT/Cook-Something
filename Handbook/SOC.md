# Handbook for SOC Tier 1

## EDR (Endpoint Detection and Response)
Là giải pháp bảo vệ thiết bị cuối, được tạo ra để khắc phục những khuyết điểm của AV truyền thống và đưa ra hiệu suất rà quét tốt hơn được sử dụng rộng rãi trong doanh nghiệp. Khác với AV truyền thống chỉ có **Signature-based** (cơ chế này gần như lỗi thời và dễ bị qua mặt bởi các malware tinh vi như Polymorphism, Obfuscate, fileless, LotL,...). Nổi trội hơn khi EDR có thêm **Behavior-based** trái ngược với triết lý phải chặn cuộc tấn công ngay từ đầu như **Signature-based** thì ở đây EDR chấp nhận rủi ro rằng sẽ không thể ngăn chặn được toàn bộ cuộc tấn công nhưng hay là nó giám sát toàn bộ cuộc tấn công và ghi lại những hành động bất thường.

### Tính năng của EDR
**Continuos Endpoint Telemetry (Thu thập dữ liệu liên tục)**: Ghi nhận mọi sự kiện ở mức **kernel** bao gồm: Process Creation, hoạt động tải về driver, sửa đổi Registry, truy cập bộ nhớ và các kết nối mạng. 

**Behavioral Analytics & Real-time Detection(Phân tích hành vi thời gian thực)**: Dùng ML và các thuật toán phân tích chuỗi sự kiện.

**Automated Response & Containment (Phản ứng và cô lập tự động)**: 
Ngay khi phát hiện điểm dị thường thì EDR có khả năng can thiệp tức thời mà không cần chờ chuyên gia xử lý --> Ngắt mạng --> Tiêu diệt tiến trình --> Cách ly tệp

**Threat Hunting**: Cung cấp công cụ truy vấn để có thể chủ động tìm kiếm các dấu hiệu của các mối đe dọa ẩn nấp dựa trên lịch sử.

**Visibility & Forensics:** Khôi phục lại chuỗi tấn công dưới dạng biểu đồ thị luồng --> Dễ phát hiện, mapping những hành động của 1 quy trình tấn công có trình tự.

## SIEM
