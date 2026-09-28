# Sensor Context & Operational Envelope

## Quan sát bối cảnh dữ liệu
- **Thiết bị:** 1 camera fisheye đơn phía trước xe (Front Fisheye ADASIND), góc rộng ~180-190 độ.
- **Biến dạng hình học:** Méo nhiều ở vùng biên (edge zone), vùng giữa (center zone) tương đối chuẩn hình dáng.
- **Vòng kính (Lens Border):** Có vành đen bao quanh góc nhìn camera fisheye ở rìa ảnh.
- **Thân xe Ego (Ego Body):** Thân xe/nắp capo/gương xe xuất hiện ở phần đáy khung hình trong 46/48 frame ADASIND.
- **Giới hạn:** 1 camera không đại diện đầy đủ cho hệ thống 4 camera SVM 360 xung quanh xe (cần kết hợp Front, Rear, Left, Right).
