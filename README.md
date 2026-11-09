# L6_L7_51 : Self Storage Application

A Python-based Self Storage application explored through software testing, code coverage analysis, and property-based fuzz testing.

This repository contains the implementations and deliverables for **Software Engineering Course – Lab 06 and Lab 07**, focusing on evaluating software quality, identifying input-validation weaknesses, and improving application reliability through systematic testing.

---

## Related Repositories

**Lab Repository:** [L6_L7_51_self_storage](https://github.com/harshithabt/L6_L7_51_self_storage)

**All SE Labs Repository:** [SE_Labs](https://github.com/harshithabt/SE_Labs)

---

## Project Overview

The Self Storage application provides basic functionality for processing storage rental information and calculating rental-related values.

The application consists of three primary functions:

- **Rental Parsing (`parse_rental`)** – Parses the storage unit and rental duration from a formatted input.
- **Duration Averaging (`duration_average`)** – Calculates the integer average of rental durations supplied as comma-separated values.
- **Payable Rent Calculation (`payable_rent`)** – Calculates the final payable rent by applying an 18% tax and subtracting the applicable discount.

The two laboratory exercises investigate different aspects of software testing using this application as the system under test.

## Laboratory Exercises

### Lab 06 — Code and Branch Coverage Analysis

**Objective:** Analyse the execution coverage of the Self Storage application and develop additional test cases to achieve comprehensive code and branch coverage.

The exercise focuses on understanding the difference between statement coverage and branch coverage and evaluating how effectively test cases exercise the application's logic.

**Work Completed:**

- Analysed the application's functions and their execution paths.
- Developed test cases using `pytest`.
- Measured statement coverage using the `coverage` Python package.
- Enabled branch coverage analysis to evaluate conditional execution paths.
- Identified uncovered statements and branches and added test cases to exercise them.
- Verified the final coverage results.

**Tools and Technologies:**
- Python
- pytest
- coverage

**Final Results:**

| Coverage Metric | Achieved |
|---|---:|
| Code / Statement Coverage | 100% |
| Branch Coverage | 100% |
| Code Coverage Test Cases | 29 passed |
| Branch Coverage Test Cases | 27 passed |

**Deliverables:**
- Code coverage test cases.
- Branch coverage test cases.
- Code coverage execution screenshot.
- Branch coverage execution screenshot.

[View Lab 06 Implementation and Deliverables](Lab06/README.md)

---

### Lab 07 — Fuzzing for Input Validation Bugs

**Objective:** Identify input-validation weaknesses in the Self Storage application using property-based fuzz testing with the Hypothesis library and improve the application to handle generated inputs safely.

Unlike conventional testing that relies on a predefined set of inputs, property-based testing generates multiple inputs automatically to explore edge cases and uncover unexpected behaviour.

**Work Completed:**

- Executed the original application using representative inputs.
- Integrated Hypothesis with pytest to generate test inputs automatically.
- Applied property-based tests to all three application functions.
- Identified failures involving empty strings, malformed input formats, missing separators, and non-string values.
- Investigated the generated failing examples.
- Updated the application with explicit input validation.
- Added checks for input types, delimiters, empty fields, and invalid numeric values.
- Ensured invalid inputs are rejected using consistent `ValueError` exceptions.
- Re-executed the application and the complete Hypothesis test suite after fixing the identified issues.

**Tools and Technologies:**
- Python
- Hypothesis
- pytest

**Final Results:**

| Testing Stage | Result |
|---|---|
| Initial Fuzz Testing | 3 test functions failed |
| Application Fixes | Input validation implemented |
| Fixed Application Execution | Successful |
| Final Hypothesis Testing | 6 tests passed |

**Deliverables:**
- Corrected Self Storage application.
- Updated Hypothesis test suite.
- Initial application execution evidence.
- Hypothesis-generated failure evidence.
- Fixed application execution evidence.
- Final passing test evidence.
- Laboratory documentation report.

[View Lab 07 Implementation and Deliverables](Lab07/README.md)

---

## Repository Structure

```text
L6_L7_51_self_storage/
│
├── README.md
│
├── Lab06/
│   ├── README.md
│   ├── .gitignore
│   ├── self_storage.py
│   ├── test_self_storage.py
│   ├── CodeCoverageTest_self_storage.py
│   ├── BranchCoverageTest_self_storage.py
│   │
│   └── screenshots/
│       ├── code_coverage.png
│       └── branch_coverage.png
│
└── Lab07/
    ├── README.md
    ├── .gitignore
    ├── requirements.txt
    ├── self_storage.py
    ├── test_self_storage.py
    ├── Lab07_Fuzz_Testing_Report.pdf
    ├── Lab07_Fuzz_Testing_Report.docx
    │
    └── screenshots/
        ├── 1_buggy_run.png
        ├── 2A_hypothesis_failures.png
        ├── 2B_failure_summary.png
        ├── 3_fixed_run.png
        └── 4_tests_passing.png
```

---

## Technologies and Tools

| Technology | Purpose |
|---|---|
| Python | Application implementation and test development |
| pytest | Test execution and test management |
| coverage | Statement and branch coverage measurement |
| Hypothesis | Property-based testing and automatic input generation |
| Git | Version control and commit management |
| GitHub | Source code hosting and repository management |

---

## Running the Tests

### Lab 06 — Coverage Analysis

Navigate to the `Lab06` directory.

Install the required packages:

```bash
python -m pip install coverage pytest
```

**Code Coverage:**

```bash
python -m coverage erase
python -m coverage run --source=self_storage -m pytest -q CodeCoverageTest_self_storage.py
python -m coverage report -m
```

**Branch Coverage:**

```bash
python -m coverage erase
python -m coverage run --branch --source=self_storage -m pytest -q BranchCoverageTest_self_storage.py
python -m coverage report -m
```

---

### Lab 07 — Fuzz Testing

Navigate to the `Lab07` directory.

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Run the Hypothesis test suite:

```bash
python -m pytest -v
```

Run the application:

```bash
python self_storage.py
```

---

## Learning Outcomes

Through these laboratory exercises, the following software testing concepts were explored:

- Understanding statement coverage and branch coverage.
- Designing test cases to exercise different execution paths.
- Measuring test effectiveness through coverage metrics.
- Understanding conventional testing versus property-based testing.
- Using automated input generation to explore edge cases.
- Identifying input-validation defects through fuzz testing.
- Implementing defensive input validation and controlled exception handling.
- Verifying application behaviour through repeated testing.

Together, Lab 06 and Lab 07 demonstrate how systematic testing can improve the reliability, correctness, and robustness of a software application.

---

## Author

**Harshitha B.T**

**SRN: PES1UG24AM118**
Section: AIML – B  

**Course:** Software Engineering 

---
