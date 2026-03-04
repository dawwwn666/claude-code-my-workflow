---
paths:
  - "**/*.py"
  - "scripts/Python/**"
---

# Python Code Standards

**Standard:** Senior Data Scientist + Financial Econometrics quality

---

## 1. Reproducibility

- `np.random.seed()` at top (YYYYMMDD format)
- `pd.set_option('display.max_columns', None)` for debugging
- All imports at top, grouped: stdlib, third-party, local
- Virtual environment: `requirements.txt` or `environment.yml`

## 2. Code Quality

- PEP 8 compliance
- Type hints for function signatures
- Docstrings (Google or NumPy style)
- `snake_case` for functions/variables, `PascalCase` for classes

## 3. Pandas Best Practices

- Avoid chained assignment (use `.loc[]` or `.iloc[]`)
- Use `.copy()` when creating derived DataFrames
- Handle missing values explicitly
- Use vectorized operations over loops

## 4. Statsmodels Conventions

- Specify formulas clearly: `'y ~ x1 + x2 + C(category)'`
- Check model diagnostics (residuals, heteroskedasticity)
- Export results to LaTeX: `model.summary().as_latex()`

## 5. Visualization Standards

```python
# Nankai University palette
NANKAI_PURPLE = '#7e0c6e'
NANKAI_GOLD = '#f2a900'
POSITIVE_GREEN = '#15803d'
NEGATIVE_RED = '#b91c1c'

# Matplotlib settings
plt.rcParams['figure.dpi'] = 300
plt.rcParams['savefig.transparent'] = True
plt.rcParams['font.size'] = 11
```

## 6. Data Export

- Pickle for Python objects: `df.to_pickle('data.pkl')`
- HDF5 for large datasets: `df.to_hdf('data.h5', key='df')`
- CSV for interoperability: `df.to_csv('data.csv', index=False)`

## 7. Financial Econometrics Pitfalls

- Check for stationarity before time series regression
- Use robust standard errors for heteroskedasticity
- Verify date alignment in panel data
- Handle outliers appropriately (winsorize vs. trim)
