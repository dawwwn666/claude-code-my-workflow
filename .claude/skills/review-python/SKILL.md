# Skill: review-python

**Trigger:** `/review-python [file]`

**Purpose:** Launch Python code reviewer agent on specified Python files.

---

## Instructions

1. Identify target Python file(s)
2. Launch `python-reviewer` agent with file path
3. Present review findings to user
4. Offer to fix critical/major issues if found

## Usage

```bash
/review-python scripts/Python/analysis.py
/review-python scripts/Python/*.py
```

## Agent Invocation

```
Agent: python-reviewer
Prompt: Review [file] for code quality, reproducibility, financial econometrics correctness, data handling, visualization quality, and performance. Provide critical/major/minor issues with line numbers.
```
