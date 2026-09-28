# Đối chiếu chất lượng cục bộ — rectangle

Teaching reference, không phải gold set đã phê duyệt; không có điểm đạt tự động.
Nguồn: export r1_craft đã khóa SHA256 `702f80251fcc7141a2ed6090b6259e3cc55e426c8e5b2e1f9da091b393b9c829`; slice `B2-dense`.
Ghép hình học greedy một-một theo IoU ≥ 0.50, rồi so class; H ≥ 40 px.
Box trái nằm chủ yếu trong ignore_region reference không tính. Polygon, polyline, track không được chấm.
Đây là phép tính offline của lab, không phải báo cáo hay kết quả tương đương CVAT Premium.

Frame được tính: adasind_062370.jpg, adasind_069450.jpg, adasind_117120.jpg. Frame thiếu trong export: không.
TP=5; FP=0; FN=15; số lần đối chiếu=20; mean IoU của TP=1.000.

| Chỉ số | Micro | Macro | Nhãn thấp nhất |
|---|---:|---:|---:|
| accuracy | 0.250 | 0.850 | 0.800 |
| precision | 1.000 | 0.400 | 0.000 |
| recall | 0.250 | 0.186 | 0.000 |
| jaccard | 0.250 | 0.186 | 0.000 |
| dice | 0.400 | 0.253 | 0.000 |

| Nhãn | TP | FP | FN | Accuracy | Precision | Recall | Jaccard | Dice |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Bike | 2 | 0 | 2 | 0.900 | 1.000 | 0.500 | 0.500 | 0.667 |
| Car | 0 | 0 | 4 | 0.800 | 0.000 | 0.000 | 0.000 | 0.000 |
| Pedestrian | 0 | 0 | 4 | 0.800 | 0.000 | 0.000 | 0.000 | 0.000 |
| ThreeWheeler | 3 | 0 | 4 | 0.800 | 1.000 | 0.429 | 0.429 | 0.600 |
| Truck | 0 | 0 | 1 | 0.950 | 0.000 | 0.000 | 0.000 | 0.000 |

| Frame | TP | FP | FN | Accuracy | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|
| adasind_062370.jpg | 5 | 0 | 4 | 0.556 | 1.000 | 0.556 |
| adasind_069450.jpg | 0 | 0 | 5 | 0.000 | 0.000 | 0.000 |
| adasind_117120.jpg | 0 | 0 | 6 | 0.000 | 0.000 | 0.000 |

Confusion matrix: hàng = teaching reference; cột = export đã khóa.
`<missing>` là thiếu box; `<extra>` là box thừa. Xem `local_quality_confusion.csv`.

| Reference \ Export | Bike | Car | Pedestrian | ThreeWheeler | Truck | <missing> |
|---|---:|---:|---:|---:|---:|---:|
| Bike | 2 | 0 | 0 | 0 | 0 | 2 |
| Car | 0 | 0 | 0 | 0 | 0 | 4 |
| Pedestrian | 0 | 0 | 0 | 0 | 0 | 4 |
| ThreeWheeler | 0 | 0 | 0 | 3 | 0 | 4 |
| Truck | 0 | 0 | 0 | 0 | 0 | 1 |
| <extra> | 0 | 0 | 0 | 0 | 0 | 0 |

Chi tiết xung đột trong `local_quality_conflicts.csv`; dữ liệu máy đọc trong `local_quality.json`.
Mismatching label đóng góp một FP cho class vẽ và một FN cho class reference; attribute khác được báo riêng.
Micro accuracy đếm mỗi cặp ghép sai class là một lần đối chiếu; Jaccard đếm cả FP và FN.
Macro/worst bỏ nhãn không xuất hiện ở cả hai phía; chỉ số không có mẫu là N/A.
