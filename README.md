# Bell-LaPadula (BLP) Access Control Visualizer

ITIS 6200 - Lab 5 (Step 1)

## Overview
This program implements and visualizes the **Bell-LaPadula (BLP)** multi-level security access control model. The model enforces two foundational confidentiality properties:
1. **Simple Security Property (No Read Up)**: A subject cannot read an object whose classification level exceeds the subject's clearance ($L(O) \le L(S)$).
2. **$\star$-Property / Star Property (No Write Down)**: A subject cannot write to an object whose classification level is lower than the subject's current security level ($L(S) \le L(O)$).
3. **Declassification Prevention**: A subject cannot unilaterally lower their security level to prevent information leakage across lower clearance domains.

## Security Levels
- `U`: Unclassified (0)
- `C`: Classified (1)
- `S`: Secret (2)
- `TS`: Top Secret (3)

## Default Subjects & Objects
- **Subjects**:
  - `alice`: Current = `U`, Max = `S`
  - `bob`: Current = `C`, Max = `C`
  - `eve`: Current = `U`, Max = `U`
- **Objects**:
  - `pub.txt`: `U`
  - `emails.txt`: `C`
  - `username.txt`: `S`
  - `password.txt`: `TS`

## How to Run
Run the interactive CLI simulator with Python 3:
```bash
python Cases.py
```
- Enter `1` through `18` to test an individual test case.
- Enter `A` to run all 18 cases sequentially.
- Enter `Q` to quit.
