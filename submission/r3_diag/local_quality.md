# Đối chiếu chất lượng cục bộ — rectangle

Teaching reference, không phải gold set đã phê duyệt; không có điểm đạt tự động.
Nguồn: export r1_craft đã khóa SHA256 `d41110eec26cd057aa042ae06545825c5cfc8a0dfdd50d9de9d0c21032ceceb0`; slice `B2-dense`.
Ghép hình học greedy một-một theo IoU ≥ 0.50, rồi so class; H ≥ 40 px.
Box trái nằm chủ yếu trong ignore_region reference không tính. Polygon, polyline, track không được chấm.
Đây là phép tính offline của lab, không phải báo cáo hay kết quả tương đương CVAT Premium.

Frame được tính: adasind_062370.jpg, adasind_069450.jpg, adasind_117120.jpg. Frame thiếu trong export: không.
TP=17; FP=4; FN=3; số lần đối chiếu=24; mean IoU của TP=0.844.

| Chỉ số | Micro | Macro | Nhãn thấp nhất |
|---|---:|---:|---:|
| accuracy | 0.708 | 0.951 | 0.917 |
| precision | 0.810 | 0.601 | 0.000 |
| recall | 0.850 | 0.601 | 0.000 |
| jaccard | 0.708 | 0.558 | 0.000 |
| dice | 0.829 | 0.601 | 0.000 |

| Nhãn | TP | FP | FN | Accuracy | Precision | Recall | Jaccard | Dice |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Bike | 4 | 0 | 0 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |
| Bus | 0 | 1 | 0 | 0.958 | 0.000 | 0.000 | 0.000 | 0.000 |
| Car | 3 | 1 | 1 | 0.917 | 0.750 | 0.750 | 0.600 | 0.750 |
| Pedestrian | 4 | 0 | 0 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |
| ThreeWheeler | 6 | 1 | 1 | 0.917 | 0.857 | 0.857 | 0.750 | 0.857 |
| Truck | 0 | 1 | 1 | 0.917 | 0.000 | 0.000 | 0.000 | 0.000 |

| Frame | TP | FP | FN | Accuracy | Precision | Recall |
|---|---:|---:|---:|---:|---:|---:|
| adasind_062370.jpg | 7 | 0 | 2 | 0.778 | 1.000 | 0.778 |
| adasind_069450.jpg | 5 | 0 | 0 | 1.000 | 1.000 | 1.000 |
| adasind_117120.jpg | 5 | 4 | 1 | 0.500 | 0.556 | 0.833 |

Confusion matrix: hàng = teaching reference; cột = export đã khóa.
`<missing>` là thiếu box; `<extra>` là box thừa. Xem `local_quality_confusion.csv`.

| Reference \ Export | Bike | Bus | Car | Pedestrian | ThreeWheeler | Truck | <missing> |
|---|---:|---:|---:|---:|---:|---:|---:|
| Bike | 4 | 0 | 0 | 0 | 0 | 0 | 0 |
| Bus | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Car | 0 | 0 | 3 | 0 | 0 | 0 | 1 |
| Pedestrian | 0 | 0 | 0 | 4 | 0 | 0 | 0 |
| ThreeWheeler | 0 | 0 | 0 | 0 | 6 | 0 | 1 |
| Truck | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| <extra> | 0 | 1 | 1 | 0 | 1 | 1 | 0 |

Chi tiết xung đột trong `local_quality_conflicts.csv`; dữ liệu máy đọc trong `local_quality.json`.
Mismatching label đóng góp một FP cho class vẽ và một FN cho class reference; attribute khác được báo riêng.
Micro accuracy đếm mỗi cặp ghép sai class là một lần đối chiếu; Jaccard đếm cả FP và FN.
Macro/worst bỏ nhãn không xuất hiện ở cả hai phía; chỉ số không có mẫu là N/A.
