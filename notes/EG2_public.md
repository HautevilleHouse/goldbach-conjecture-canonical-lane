# EG2 Public Note

Gate: `GB_G2`
Constant: `sigma_minor_arc`

This note isolates the capture package. The defect functional `D_tau` obeys a local-to-global inequality with explicit continuous and restart losses. The extracted theorem-level constant is `sigma_minor_arc > 0`, obtained from the raw formula

`minor_arc_floor_raw - decomposition_loss_raw - truncation_loss_raw`.

The gate closes when the admissible flow preserves a strictly positive defect floor after subtracting every tracked loss term.
