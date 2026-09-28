# So sánh L với R

Chỉ số L/R là thứ tự box cao ≥ H=40 trong từng frame, theo thứ tự XML; bắt đầu từ 1.
Box L trong ignore_region được báo IGNORE_SCOPE, không tính SPURIOUS.

## adasind_062370.jpg
- L7 edge IGNORE_SCOPE
- R7 center MISSING
- R8 center MISSING
## adasind_069450.jpg
- L3 edge IGNORE_SCOPE
## adasind_117120.jpg
- L1 edge IGNORE_SCOPE
- L5 center SPURIOUS
- L7 mid SPURIOUS
- L9 center SPURIOUS
- L10 center SPURIOUS
- R3 center MISSING

## Theo zone
| zone | n_ref | matched | missing | spurious |
|---|---|---|---|---|
| center | 13 | 10 | 3 | 3 |
| mid | 5 | 5 | 0 | 1 |
| edge | 2 | 2 | 0 | 0 |
