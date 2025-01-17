### Bối cảnh và mục tiêu:
- Trực tuyến đóng vai trò quan trọng trong việc ảnh hưởng đến quyết định của người tiêu dùng và uy tín doanh nghiệp.
Sự xuất hiện của các đánh giá giả mạo gây thách thức lớn, ảnh hưởng đến tính toàn vẹn của nền tảng.
- Mô hình đã huấn huấn luyện thể được tải và triển khai để dự đoán trên từng batch dữ liệu từ Spark Streaming cho dự án này.
### Phương pháp:

- Sử dụng bộ dữ liệu YelpChi, tập dữ liệu chứa hơn 67.000 đánh giá từ 38.000 người dùng và 201 khách sạn/nhà hàng.
- Biểu diễn đồ thị với 3 loại quan hệ: đánh giá cùng người dùng, cùng sản phẩm (cùng đánh giá sao), và cùng thời điểm.
- Triển khai GraphSAGE (một mô hình GNN dành cho đồ thị lớn) và CARE-GNN (một mô hình GNN tối ưu cho phát hiện gian lận).
### Kết quả:
Cả hai mô hình đều hiệu quả trong phát hiện gian lận:
- GraphSAGE đạt độ chính xác 85%, nhưng gặp khó khăn với các nút được "ngụy trang".
- CARE-GNN đạt ROC-AUC 0,76 và Recall 0,70, hiệu quả hơn trong việc phát hiện nhóm gian lận phối hợp.
- CARE-GNN yêu cầu tinh chỉnh nhiều hơn và có độ phức tạp tính toán cao hơn.
### Ưu điểm & Hạn chế:

- Ưu điểm: Tăng độ tin cậy của các hệ thống đánh giá trực tuyến, hỗ trợ phát hiện hành vi gian lận hiệu quả.
- Hạn chế: Tập dữ liệu không đại diện hoàn toàn cho các ngành và nền tảng khác; yêu cầu tài nguyên tính toán lớn.
### Kết luận và hướng phát triển:

Nghiên cứu đóng góp vào việc phát triển hệ thống đánh giá đáng tin cậy, giúp người tiêu dùng đưa ra quyết định thông minh và bảo vệ uy tín doanh nghiệp.
Hướng nghiên cứu tương lai bao gồm mở rộng tập dữ liệu, tối ưu hóa hiệu quả tính toán, và kết hợp phương pháp đồ thị với máy học truyền thống.
