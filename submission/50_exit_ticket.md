# Exit Ticket — Tổng kết Buổi Lab Day 11

## 1. Quản lý Identity và Keyframe trong 1 Camera
- Khi vật thể di chuyển trong 1 camera, giữ nguyên track ID và sử dụng Outside khi vật đi ra khỏi góc nhìn.

## 2. Xử lý Vùng chồng (Seams) giữa các Camera
- Hai box xuất hiện ở vùng overlap của 2 camera là hợp lệ nếu bám đúng hình học fisheye của camera đó. Chỉ thực hiện nối track liên camera khi có đủ Calibration, Timestamp và Policy Output.

## 3. Bài học Tự nhìn lại (Self-Reflection)
- Qua việc gán nhãn và đối chiếu trên Slice `B2-dense`, bài học lớn nhất là cần tuân thủ nghiêm ngặt rule H=40 và tách biệt rõ thuộc tính `truncated` (do mép/kính) với `occluded` (do vật che).
