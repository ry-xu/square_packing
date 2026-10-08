We achieve these results through LLM-driven evolutionary program search, similar to AlphaEvolve.

The programs were seeded with primitives vibe-coded by yours truly, and the search was lightly guided between meetings and on insufficient sleep.

Coordinates can be found in square_packing_records.json

New records:
<img width="3600" height="2340" alt="download" src="https://github.com/user-attachments/assets/0cedc84f-6c80-4f2a-a7ae-fe19465c62f9" />

## Certificates

Each record has an exact certificate in [`certificates/nNNN/`](certificates):

- `nNNN.cert.json`: exact rational packing, with side `s_exact` and, per square, a rational centre `(x, y)` and a rational
  `t = tan(θ/2)`, so `(cos θ, sin θ) = ((1−t²)/(1+t²), 2t/(1+t²))` holds exactly and every square is an exact unit square.
- `nNNN.cert.txt`: the same packing in David Ellsworth's text format (box centred at the origin, degrees, 40 digits).
- `nNNN.witness.yaml`: the same packing as a jlevy/squares `Witness/v2` (decimal centre–angle, 40 digits).
- `nNNN_vs_record.png`: the previous record (jlevy/squares register as of 2026-10-06) and our packing, to one scale.
- `check_output.txt`: the outputs of the checkers that accepted it: an exact rational checker, David Ellsworth's
  `check_packing.py` at precision 40, and jlevy/squares `packing-witness` check, promote and exact verify.

The certificates are built from `square_packing_records.json`: angles become rational half-angle tangents and the packing is
dilated about the box centre by `1 + 10⁻¹²` (raising each side by at most 2·10⁻¹¹). n = 51 is also exact at
`s = (16 + 5√2)/3`, from the exact coordinates in `square_packing_records.json`. These are upper bounds `s(n) ≤ s_exact`, not proofs of optimality.
