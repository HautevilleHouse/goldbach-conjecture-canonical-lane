# EG2 Public Note (Capture and Restart)

Mature wording: `transport / local-to-global transfer`.

In-paper anchor: `paper/GOLDBACH_CONJECTURE_PREPRINT.md` (`GB_G2`).

## Goal
Expand the compressed capture/restart language into the local-to-global transport gate for `prove the binary Goldbach statement by routing admissible circle-method states through major-arc coercivity, minor-arc capture, compactness, rigidity, prime-pair transfer, and strict coherence`.

## Objects

- transport carrier: the admissible evolution, deformation, or routed lattice declared in the preprint.
- capture floor: `sigma_minor_arc`.
- restart law: the normalization/re-entry rule that keeps corrective steps inside the admissible class.
- carried losses: defect, restart, and normalization losses that must remain explicit.

## Closure Criterion

`GB_G2` closes when `sigma_minor_arc` survives admissible losses and restart corrections: minor-arc defect stays above capture floor across decomposition and truncation losses.
This is the transport contribution to `M_GB`.

## Lemma Chain and Proof Payload

### Lemma EG2.1 (transport accounting)
Every transport step used by the lane is charged to the declared defect ledger instead of being absorbed into prose.

Payload: check that the capture constant `sigma_minor_arc` is present in the constants registry and extraction inputs.

### Lemma EG2.2 (restart preservation)
Restart or normalization preserves the declared admissible class and does not create an untracked remainder.

Payload: inspect the repro script and guard output for the gate tied to `sigma_minor_arc`.

### Theorem EG2.3 (capture gate closure)
If transport accounting and restart preservation hold, then `GB_G2` carries local control forward without breaking admissibility.

## Current Instantiation

- gate: `GB_G2`
- artifact key: `sigma_minor_arc`
- mature equivalent: `transport / local-to-global transfer`
- audit surface: `repro/run_repro.sh` and `repro/certificate_runtime.json`
