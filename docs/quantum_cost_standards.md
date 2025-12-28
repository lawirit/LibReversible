# Quantum Cost Standards

This document defines the quantum cost for primitive reversible gates used in the library.

## Primitive Gate Costs

| Gate | Quantum Cost | Description |
|------|--------------|-------------|
| CNOT | 1 | Controlled-NOT (Feynman gate) |
| Toffoli | 5 | Controlled-Controlled-NOT (CCNOT) |
| Fredkin | 7 | Controlled-SWAP |
| Peres | 4 | Peres gate (1 Toffoli + 1 CNOT) |
| TR | 3 | Toffoli with relative phase |
| R | 2 | Rotation gate |

## Circuit Quantum Cost Calculation

The quantum cost of a reversible circuit is the sum of the quantum costs of all primitive gates in its decomposition into a universal gate set (usually CNOT, Toffoli, and single-qubit gates).

## Example: 4x4 Reversible Multiplier

### Original Implementation
- **File**: `src/multipliers/rev_4x4_multiplier.v`
- **Quantum Cost**: 85
- **Gate Count**: 16 Toffoli, 12 CNOT, 4 Fredkin
- **Garbage Outputs**: 8
- **Description**: Standard array multiplier using reversible AND gates (Toffoli) and reversible full adders.

### Optimized Implementation
*To be added after optimization.*