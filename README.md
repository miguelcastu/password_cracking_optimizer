# Password Auditing Lab — Synthetic Hash Experiments

A historical Python exercise generating synthetic password/hash datasets and
exploring authorized offline recovery with John the Ripper. The accompanying
Spanish DOCX records the original experiment; it is not a benchmark independently
reproduced by this portfolio audit.

[Engineering portfolio](https://github.com/miguelcastu/miguelcastu) · [Project directory](https://github.com/miguelcastu/miguelcastu/blob/main/PROJECTS.md)

## Implementation

| File | Purpose |
| --- | --- |
| `generador_md5.py` | Random synthetic strings and raw MD5 digests |
| `generador_sha256.py` | Random synthetic strings and SHA-256 digests |
| `generador_sha3.py` | Random synthetic strings and SHA3-256 digests |
| `generador_diccionario_sha256.py` | Wordlist-based mutations and SHA-256 datasets |
| `pruebas.py` | Small exploratory scratch script, not an automated test suite |

The generators use Python's standard library and write paired plaintext/hash files
to the current working directory. Inspect dataset sizes and output paths before
running; the wordlist variant requires an external dictionary. The source is not
a packaged CLI and does not provide a reproducible performance benchmark.

Use only synthetic values or hashes explicitly authorized for an offline audit.
Raw MD5/SHA-family hashing and `random` are study mechanisms, not suitable designs
for production password storage or cryptographic password generation. No recovery
rate, optimization guarantee or real credential result is claimed.
