# Interlock

On-chain decision interlock on X Layer / TapeOut.

The gate opens only when the signal is on AND spare capacity remains.

- Processor: `0x163C980ee0E9eccc142fED1dfdbb902e89da9814`
- Circuit ID: `1.2.238`
- Wallet: `0xe13a4ca61a0f3f72709668be265856180f1469c4`
- Tapeout tx: https://www.oklink.com/xlayer/tx/0xdfabb80efb3468eabd08bbeaff478f31e05980887c43d44f83f37bff5c654e56

## Truth table

| A signal | B spare | OUT |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |
