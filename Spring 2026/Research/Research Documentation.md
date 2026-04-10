


Split observables into 2 classes:
- Computational observables (Quantum Computers can find these)
- Theoretical observables (Classical exact state needed)




## Different Matrix Exponentiation

| # Qubits | `expm`     | `sparse.expm` | `expm_multiply` | `expm_multiply` with `sparse=true` |
| -------- | ---------- | ------------- | --------------- | ---------------------------------- |
| 2        | 30.513 ms  | 52.733 ms     | 47.801 ms       | 123.533 ms                         |
| 3        | 44.153 ms  | 61.976 ms     | 58.018 ms       | 144.108 ms                         |
| 4        | 50.341 ms  | 73.991 ms     | 68.984 ms       | 119.283 ms                         |
| 5        | 59.355 ms  | 169.347 ms    | 77.771 ms       | 114.457 ms                         |
| 6        | 60.336 ms  | 226.638 ms    | 227.100 ms      | 115.037 ms                         |
| 7        | 77.795 ms  | 416.738 ms    | 310.254 ms      | 129.969 ms                         |
| 8        | 270.656 ms | 2.064 s       | 542.760 ms      | 118.990 ms                         |
| 9        | 736.168 ms | 6.920 s       | 1.327 s         | 136.970 ms                         |
| 10       | 2.348 s    | 33.221 s      | 3.997 s         | 158.772 ms                         |
| 11       | 8.055 s    | -             | 13.730 s        | 173.241 ms                         |
| 12       | 31.840 s   | -             | 57.948 s        | 217.209 ms                         |
| 13       |            |               |                 | 298.042 ms                         |
| 14       |            |               |                 | 492.460 ms                         |
| 15       |            |               |                 | 1.063 s                            |
| 16       |            |               |                 | 2.581 s                            |
| 17       |            |               |                 | 5.377 s                            |
| 18       |            |               |                 | 10.532 s                           |
| 19       |            |               |                 | 21.165 s                           |
| 20       |            |               |                 | 42.137 s                           |
| 21       |            |               |                 | 91.707 s                           |
| 22       |            |               |                 | 184.157 s                          |
For 101 points each.
