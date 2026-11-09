# Lab 07: Fuzz Testing: Self Storage

---

**Lab Repository:** [L6_L7_51_self_storage](https://github.com/harshithabt/L6_L7_51_self_storage)

**All SE Labs Repository:** [SE_Labs](https://github.com/harshithabt/SE_Labs)

---

This lab applies property-based fuzz testing to the Self Storage input-processing functions using Hypothesis. Generated inputs exercise valid values, malformed strings, missing separators, non-text values, empty fields, and numeric edge cases. Invalid inputs are rejected with a consistent `ValueError` rather than leaking parsing or arithmetic exceptions.

## What was covered

- Property-based testing with Hypothesis
- Generated valid and malformed inputs
- Boundary values and numeric edge cases
- Separator and field validation
- Consistent error handling
- Regression checks for valid calculations

## Files

| File | Description |
|---|---|
| `self_storage.py` | Input parsing and rental calculation functions with validation |
| `test_self_storage.py` | Hypothesis property-based fuzz tests |
| `requirements.txt` | Test dependencies |

## Install dependencies

```bash
python -m pip install -r requirements.txt
```

## Run fuzz tests

```bash
python -m pytest -v
```

Hypothesis generates and shrinks test examples. The tests verify that valid inputs preserve the expected calculations and malformed inputs are rejected with `ValueError`.

## Project Structure 

```bash
Lab07/
│
├── README.md
├── .gitignore
├── requirements.txt
├── self_storage.py
├── test_self_storage.py
├── Lab07_Fuzz_Testing_Report.pdf
│
└── screenshots/
    ├── code_coverage.png
    └── branch_coverage.png
```

## Author

Harshitha B.T. – PES1UG24AM118 (AIML-B Section)

Course: Software Engineering 

---
