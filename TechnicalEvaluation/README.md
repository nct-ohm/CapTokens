# CapTokens
CapTokens: Authentication Through 3D-Printed Tangibles with Hidden Conductive Structures

# Recognition Evaluation Dataset

This repository contains the raw trial-level recognition results collected during the evaluation of the tangible key recognition prototype (`com.example.tangible_recognition_v1`).

## Contents

| File | Description |
|---|---|
| `CapTokenEval.xlsx` | Trial-level recognition results, exported from the application's debug log. Contains three sheets, one per evaluation condition (see below). |
| `LICENSE` | License governing reuse of the dataset. |

## Study design / conditions

The workbook contains three sheets, one per evaluation condition:

| Sheet | n (trials) | Condition | Description |
|---|---|---|---|
| `BlockA_NEW correct` | 100 | `correct` | participant entered the intended/correct key sequence |
| `BlockB_NEW false` | 100 | `false` | participant entered a deliberately incorrect key sequence |
| `BlockC_NEW fast` | 50 | `fast` | participant entered the key sequence under fast condition |

## Column description

Each sheet contains the same six (unlabeled) columns, in this order:

| Column | Description |
|---|---|
| 1 | Timestamp of the logged event (`yyyy-MM-dd HH:mm:ss[.SSS]`, optionally followed by a process/thread ID). |
| 2 | Log tag (`CAPKEY_EVAL`). |
| 3 | Application package name (`com.example.tangible_recognition_v1`). |
| 4 | Android log level (`D` = debug). |
| 5 | Result field: `RESULT: Recognized` or `RESULT: Not Recognized`. |
| 6 | Input length field: `LENGTH: <n>`, where `<n>` is the length of the input sequence as reported by the application. `LENGTH: 0` indicates an empty/no input was registered for that trial. |

## Data provenance and processing notes

- Data were exported from the application's debug log (Android Logcat, package `com.example.tangible_recognition_v1`).
- All 250 trials were collected from a single participant (Fabian Mai), across two recording sessions (2026-05-19 and 2026-06-12/13). This dataset reflects a single-subject evaluation, not a multi-participant user study
