# L / R / M

L/R/M là thứ tự box in-scope theo XML của từng frame.

## adasind_062370.jpg
- L1+R1: LR_noM (mid)
- L2+R2+M2: LRM (center)
- L3+R3+M9: LRM (edge)
- L4+R6: LR_noM (center)
- L5+R7: LR_noM (center)
- R4+M6: RM_noL (mid)
- R5: R_only (center)
- R8: R_only (center)
- R9+M7: RM_noL (center)
- M3: M_only (center)
- M4: M_only (edge)
- M5: M_only (center)
- M8: M_only (mid)
- M10: M_only (center)
## adasind_069450.jpg
- R1: R_only (edge)
- R2: R_only (mid)
- R3+M3: RM_noL (center)
- R4+M4: RM_noL (center)
- R5+M6: RM_noL (center)
- M5: M_only (edge)
- M7: M_only (mid)
## adasind_117120.jpg
- R1+M3: RM_noL (mid)
- R2: R_only (center)
- R3+M5: RM_noL (center)
- R4: R_only (center)
- R5+M2: RM_noL (mid)
- R6+M4: RM_noL (center)
- M1: M_only (center)
- M6: M_only (mid)
- M7: M_only (center)
- M8: M_only (center)
- M10: M_only (center)

## Zone × cell
| zone | LRM | LR_noM | LM_noR | L_only | RM_noL | R_only | M_only |
|---|---|---|---|---|---|---|---|
| center | 1 | 2 | 0 | 0 | 6 | 4 | 7 |
| mid | 0 | 1 | 0 | 0 | 3 | 1 | 3 |
| edge | 1 | 0 | 0 | 0 | 0 | 1 | 2 |
