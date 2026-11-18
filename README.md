# UK Tax Rates & Statutory Thresholds (2026/27 Tax Year) — Open Dataset

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Format: JSON & CSV](https://img.shields.io/badge/Format-JSON%20%7C%20CSV-success.svg)]()
[![Source: GOV.UK Verified](https://img.shields.io/badge/Source-GOV.UK%20Verified-brightgreen.svg)]()

Comprehensive, machine-readable open data covering official **HM Revenue & Customs (HMRC)** and **Scottish Government** income tax bands, Class 1 National Insurance thresholds, and Student Loan repayment parameters for the **2026/27 UK tax year**.

Maintained as an open-data asset by **[Take Home Pay Calculator UK](https://takehomepaycalculatoruk.com)**.

---

## Interactive Web Tools & Calculators

If you are looking for ready-to-use payroll calculators rather than raw data files, visit the official live tools:

* 🧮 **[Take-Home Pay Calculator UK](https://takehomepaycalculatoruk.com)** — Flagship after-tax salary calculator for England, Wales & Northern Ireland.
* 🏴󠁧󠁢󠁳󠁣󠁴󠁿 **[Scottish Take-Home Pay Calculator](https://takehomepaycalculatoruk.com/scotland/take-home-pay-calculator/)** — Full 6-tier Scottish progressive income tax breakdown.
* 📊 **[Official 2026/27 UK Tax Rates & Bands](https://takehomepaycalculatoruk.com/tax-rates/)** — Complete rate schedules and statutory citations.
* 🛡️ **[How to Avoid the 60% Tax Trap](https://takehomepaycalculatoruk.com/guides/60-percent-tax-trap/)** — Pension sacrifice guide for earnings between £100,000 and £125,140.
* 💰 **[Salary Calculator UK](https://takehomepaycalculatoruk.com/salary-calculator/)** — Instant annual, monthly, and hourly payroll breakdowns.
* 📉 **[National Insurance Calculator](https://takehomepaycalculatoruk.com/national-insurance-calculator/)** — Class 1 employee & employer NI computations.

---

## Dataset Structure

All data files are located in the [`/data/`](./data/) directory in both JSON and CSV formats:

| File | Description | Format |
|---|---|---|
| [`data/income-tax-bands-2026.json`](./data/income-tax-bands-2026.json) | England, Wales & NI tax bands & personal allowance taper | JSON |
| [`data/scotland-tax-bands-2026.json`](./data/scotland-tax-bands-2026.json) | Scottish 6-band income tax schedule | JSON |
| [`data/national-insurance-2026.json`](./data/national-insurance-2026.json) | Class 1 Primary & Upper thresholds, rates | JSON |
| [`data/student-loan-thresholds-2026.json`](./data/student-loan-thresholds-2026.json) | Plans 1, 2, 4, 5 and Postgraduate repayment limits | JSON |
| [`data/uk-tax-rates-2026.csv`](./data/uk-tax-rates-2026.csv) | Consolidated flat tabular data across all jurisdictions | CSV |

---

## Quick Usage

### Python (Pandas)
```python
import pandas as pd

df = pd.read_csv("https://raw.githubusercontent.com/mraqeelpkorg-glitch/uk-tax-rates-2026-dataset/main/data/uk-tax-rates-2026.csv")
print(df[df["Jurisdiction"] == "England/Wales/NI"])
```

### Node.js / JavaScript
```javascript
const rukBands = require('./data/income-tax-bands-2026.json');
console.log(rukBands.tax_bands);
```

---

## 2026/27 Tax Year Summary

### 1. Income Tax (England, Wales, NI)
* **Personal Allowance:** £12,570 (frozen). Withdrawn £1 for every £2 of income between £100,000 and £125,140.
* **Basic Rate (20%):** £12,571 to £50,270
* **Higher Rate (40%):** £50,271 to £125,140
* **Additional Rate (45%):** Above £125,140

### 2. Scottish Devolved Income Tax
* **Starter Rate (19%):** £12,571 to £14,876
* **Basic Rate (20%):** £14,877 to £26,561
* **Intermediate Rate (21%):** £26,562 to £43,662
* **Higher Rate (42%):** £43,663 to £75,000
* **Advanced Rate (45%):** £75,001 to £125,140
* **Top Rate (48%):** Above £125,140

### 3. Class 1 National Insurance
* **Primary Threshold:** £12,570/yr (0% employee NI)
* **Main Band (8%):** £12,571 to £50,270/yr
* **Upper Band (2%):** Above £50,270/yr

---

## Attribution & License

Released under the **MIT License**. Created by the open-source team behind **[TakeHomePayCalculatorUK.com](https://takehomepaycalculatoruk.com)**.
