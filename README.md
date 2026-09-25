# Interlock

On-chain decision interlock on X Layer / TapeOut.

Two circuits on one processor.
The simple gate opens when both keys are on.
The breaker remembers a trip and stays closed until reset.

- Processor: `0x163C980ee0E9eccc142fED1dfdbb962e89da9814`
- Circuit 1 (instant AND): `1.2.238`
- Circuit 2 (dual-key breaker): `2.2.238`
- Wallet: `0xe13a4ca61a0f3f72709668be265856180f1469c4`
- Circuit 1 tx: https://www.oklink.com/xlayer/tx/0xdfabb80efb3468eabd08bbeaff478f31e05980887c43d44f83f37bff5c654e56
- Circuit 2 tx: https://www.oklink.com/xlayer/tx/0x6422a47f1e1934656dfea90bd908dc200b3c93784fe938116bd7bc2ca943c0c3

## Circuit 2 inputs

- IN0 HUMAN
- IN1 RISK
- IN2 SAFE
- IN3 RESET
- OUT allow action

## Circuit 2 checks

| HUMAN | RISK | SAFE | RESET | note | OUT |
| --- | --- | --- | --- | --- | --- |
| 1 | 1 | 1 | 0 | both keys, healthy | 1 |
| 1 | 1 | 0 | 0 | trip | 0 |
| 1 | 1 | 1 | 0 | healthy again, still latched | 0 |
| 1 | 0 | 1 | 0 | missing risk key | 0 |
