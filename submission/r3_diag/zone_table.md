# Zone table (slice của bạn)

Lệnh `python3 lab11.py model` tự ghi bảng số (cùng cách đếm với `r1_craft/compare.md` và `model_compare.md`); chạy lại lệnh sẽ cập nhật bảng và giữ nguyên phần nhận xét. Bạn chỉ viết mục Nhận xét.

| Zone | n_ref | L missing | L spurious | M missing (`LR_noM` + `R_only`) | M thừa (`LM_noR` + `M_only`) | Lỗi L chính (`what`) |
|---|---:|---:|---:|---:|---:|---|
| center | 13 | 3 | 3 | 6 | 7 | MISSING (3) |
| mid | 5 | 0 | 1 | 2 | 3 | SPURIOUS (1) |
| edge | 2 | 0 | 0 | 1 | 2 | — |

## Nhận xét Chẩn đoán
- **Zone gãy nhiều nhất:** Vùng `center` có số lượng missing và spurious cao nhất do mật độ đối tượng tập trung dày đặc.
- **Giả thuyết nguyên nhân:** YOLO model bị ảnh hưởng bởi độ phân giải và hiện tượng méo fisheye nhẹ ở ranh giới giữa center và mid.
- **Giới hạn Slice:** Tập dữ liệu 3 frame ADASIND mang tính chất đại diện mô phỏng, chưa bao quát hết mọi điều kiện thời tiết và ánh sáng phức tạp.
