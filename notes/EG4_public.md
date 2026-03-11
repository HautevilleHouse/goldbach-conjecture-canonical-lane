# EG4 Public Note

Gates: `GB_G4`, `GB_G5`
Constants: `rho_rigidity`, `prime_pair_transfer`

This note packages rigidity and transfer. Rigidity excludes the bad-limit class by contradiction with the admissible identities, while the transfer inequality carries the rigid endpoint into the intended target class. The extracted theorem-level constants are `rho_rigidity > 0` and `prime_pair_transfer > 0`, obtained from

- `rho_rigidity_raw`
- `c_pair_raw * rigidity_transfer_raw - e_pair_raw`

Together these gates block spurious endpoint models and preserve the intended target structure.
