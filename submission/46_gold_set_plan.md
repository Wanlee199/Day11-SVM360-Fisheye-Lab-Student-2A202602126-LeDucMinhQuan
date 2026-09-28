# Kế hoạch Thiết lập Gold Set 4 Camera

## Tiêu chuẩn Chọn mẫu Gold Set
- Chọn các frame bao gồm cả trường hợp Normal và Hard cho 4 camera.
- Đảm bảo 2 Chuyên gia QA độc lập thẩm định và đạt độ nhất trí IoU > 0.85 trước khi khóa làm Gold Set.

## Xử lý Vùng chồng (Seam Overlaps)
- Tại vùng seam giữa 2 camera (ví dụ Front và Left), vật thể xuất hiện ở cả 2 ảnh được gán box độc lập theo luật hình học từng camera, không tự ý gộp track ID khi chưa có thông số Calibration và Timestamp đồng bộ.
