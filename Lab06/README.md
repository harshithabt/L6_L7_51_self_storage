# Lab 06: Code and Branch Coverage: Self Storage

---

**Lab Repository:** [L6_51_self_storage](https://github.com/harshithabt/L6_51_self_storage/tree/main)

**All SE Labs Repository:** [SE_Labs](https://github.com/harshithabt/SE_Labs)

---

This lab focuses on analysing statement (line) coverage and branch coverage for the supplied Self Storage application. The instructor-provided application is preserved; additional test cases exercise the functions and their decision outcomes.

## What was covered

- Statement (line) coverage
- Branch coverage
- Boundary and edge-case testing
- Positive and negative decision outcomes
- Coverage measurement using `coverage.py` and `pytest`

## Files

| File | Description |
|---|---|
| `self_storage.py` | Original application under test; unchanged |
| `CodeCoverageTest_self_storage.py` | Test cases targeting statement/line coverage |
| `BranchCoverageTest_self_storage.py` | Test cases targeting both outcomes of decision branches |

## Install dependencies

```bash
python -m pip install pytest coverage
```

## Run statement coverage

```bash
coverage erase
coverage run --source=self_storage -m pytest -q CodeCoverageTest_self_storage.py
coverage report -m
```

## Run branch coverage

```bash
coverage erase
coverage run --branch --source=self_storage -m pytest -q BranchCoverageTest_self_storage.py
coverage report -m
```

## Project Structure 

```bash
L6_51_self_storage/
│
├── README.md
├── .gitignore
├── self_storage.py
│
├── CodeCoverageTest_self_storage.py
├── BranchCoverageTest_self_storage.py
│
└── screenshots/
    ├── code_coverage.png
    └── branch_coverage.png
```

## Verified results

The test suites were run against the original application without modifying `self_storage.py`.

| Measurement | Tests passed | Coverage |
|---|---:|---:|
| Statement/line coverage | 29 | 100% |
| Branch coverage | 27 | 100% |

Capture terminal screenshots of each final coverage report on the machine used for submission. The lab handout requests screenshots showing at least 90% coverage.

## Author

Harshitha B.T. – PES1UG24AM118 (AIML-B Section)

Course: Software Engineering   

---