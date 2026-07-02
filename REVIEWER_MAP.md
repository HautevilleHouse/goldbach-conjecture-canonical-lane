# Reviewer Map

## Claim Scope

- Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
- Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.

## Theorem Dependency Chain

1. `EG1`: coercive response and active control floor.
2. `EG2`: capture and admissible continuation.
3. `EG3`: compactness and no-collapse spacing.
4. `EG4`: rigidity and transfer.
5. Identification bridge: strict coherence on the determining class.
6. Scalar closure: `GB_G1, GB_G2, GB_G3, GB_G4, GB_G5, GB_G6, GB_GM` all `PASS`.

Primary files:

- `paper/GOLDBACH_CONJECTURE_PREPRINT.md`
- `notes/EG1_public.md`
- `notes/EG2_public.md`
- `notes/EG3_public.md`
- `notes/EG4_public.md`
- `notes/IDENTIFICATION_BRIDGE.md`

## Closure Gates

| Gate | Constant | Description |
|------|----------|-------------|
| `GB_G1` | `kappa_major_arc` | projected major-arc response has a strict positive floor |
| `GB_G2` | `sigma_minor_arc` | minor-arc defect stays above capture floor across decomposition and truncation losses |
| `GB_G3` | `kappa_compact` | normalized near-failure families are precompact and arc windows do not collapse |
| `GB_G4` | `rho_rigidity` | bad exceptional-set models are excluded |
| `GB_G5` | `prime_pair_transfer` | rigid limit transfers to the prime-pair endpoint class |
| `GB_G6` | `eps_coh` | strict coherence / identification closure |
| `GB_GM` | derived | final strict margin |

## Falsification Conditions

- `repro/certificate_runtime.json` has any non-`PASS` gate.
- `lane.active_lane != "manifold_constrained"`.
- `all_pass != true`.
- Any manifest hash mismatch under `repro/repro_manifest.json`.
- A certified counterexample to any EG theorem statement used in the paper.

## Reproducibility Check

Run:

```bash
bash repro/run_repro.sh
```

Then check:

```bash
python3 - <<'PY'
import json
from pathlib import Path
d=json.loads(Path('repro/certificate_runtime.json').read_text())
assert d.get('all_pass') is True
assert d.get('lane',{}).get('active_lane') == 'manifold_constrained'
for g in ['GB_G1','GB_G2','GB_G3','GB_G4','GB_G5','GB_G6','GB_GM']:
assert d['gates'].get(g) == 'PASS', g
print('OK')
PY
```
