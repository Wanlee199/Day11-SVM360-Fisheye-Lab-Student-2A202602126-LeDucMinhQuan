# Báo cáo Phân vùng Chẩn đoán Zone Table

## Nhận xét Chẩn đoán
- **Zone gãy nhiều nhất:** Vùng `center` có số lượng missing và spurious cao nhất do mật độ đối tượng tập trung dày đặc.
- **Giả thuyết nguyên nhân:** YOLO model bị ảnh hưởng bởi độ phân giải và hiện tượng méo fisheye nhẹ ở ranh giới giữa center và mid.
- **Giới hạn Slice:** Tập dữ liệu 3 frame ADASIND mang tính chất đại diện mô phỏng, chưa bao quát hết mọi điều kiện thời tiết và ánh sáng phức tạp.
