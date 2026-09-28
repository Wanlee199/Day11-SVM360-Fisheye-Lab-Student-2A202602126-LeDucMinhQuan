# Báo cáo Quan sát Vạch Bãi Đỗ (Parking Lot)

## Các vạch đã chọn làm `parking_line`
- Hai dải sơn màu trắng ở tiền cảnh phân chia trực tiếp từng ô đỗ riêng biệt.
- Vạch vẽ chạy bám theo ranh giới phần sơn nhìn thấy thật trên ảnh lõi (`parking-lot-core.jpg`).

## Vạch/Biên đã loại trừ
- Biên vạch chỉ dẫn đường xe chạy ở dải đường giữa và mép đường xa không phải là vạch chia ô đỗ nên không gán `parking_line`.

## Ranh giới `free_space`
- Polygon `free_space` bao phủ vùng mặt đường lối xe chạy trống giữa hai hàng ô đỗ ở tiền cảnh, dừng lại trước các xe đỗ và mép curb.
