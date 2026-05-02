# Methodology — Kyrgyzstan Banking Analysis 2024

## Data model
This project uses a **long-format data model** — one row per bank per metric per year.
Shape: 286 rows × 5 columns (`bank_code`, `bank_name`, `metric`, `year`, `value`).
The wide-to-long transformation was performed in Power Query using the Unpivot Other Columns operation.

## Units
All monetary values are in **millions of KGS**.
Banks reporting in thousands were divided by 1,000 during extraction.

## Statements used per bank
| Bank | PDF file | Statements used |
|---|---|---|
| Aiyl Bank | AB.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Bai Tushum | Bai Tushum.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Bakai Bank | Bakai Bank.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Capital Bank | Capital Bank 2023.pdf, Capital Bank 2024.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Companion Bank | Companion Bank.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Demir Bank | Demir 2023.pdf, Demir 2024.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Doscredo Bank | Doscredo Bank 2023.pdf, Doscredo Bank 2024.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Eldik Bank | Eldik Bank.PDF | Statement of Financial Position, Statement of Comprehensive Income |
| KICB | KICB.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| KKB | KKB.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Keremet Bank | Keremet Bank.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| MBANK | MBANK.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Optima Bank | Optima-Bank.pdf | Statement of Financial Position, Statement of Comprehensive Income |

## Raw metrics collected
| Metric name (in dataset) | Description | Source statement |
|---|---|---|
| total_assets | Total assets | Statement of Financial Position |
| total_liabilities | Total liabilities | Statement of Financial Position |
| equity | Total equity | Statement of Financial Position |
| loans | Loans and advances to customers (net) | Statement of Financial Position |
| deposits | Customer accounts | Statement of Financial Position |
| interest_income | Interest income | Statement of Comprehensive Income |
| interest_expense | Interest expense (negative value) | Statement of Comprehensive Income |
| net_interest_income | Net interest income before provisions | Statement of Comprehensive Income |
| operating_income | Total operating income | Statement of Comprehensive Income |
| operating_expenses | Operating expenses (negative value) | Statement of Comprehensive Income |
| net_profit | Profit for the period | Statement of Comprehensive Income |

## Derived metrics (DAX measures)
| Measure | Formula | Notes |
|---|---|---|
| ROA | net_profit / total_assets | End-of-period assets used |
| ROE | net_profit / equity | End-of-period equity used |
| CIR | ABS(operating_expenses) / operating_income | ABS used because expenses stored as negative |
| Equity to Assets | equity / total_assets | Capital adequacy proxy |
| Asset Growth | (total_assets_2024 - total_assets_2023) / total_assets_2023 | YoY change |
| Profit Growth | (net_profit_2024 - net_profit_2023) / net_profit_2023 | YoY change |
| Loan Growth | (loans_2024 - loans_2023) / loans_2023 | YoY change |

## Composite score methodology
Banks are ranked using a weighted composite score (0–1 scale, higher = better).

Each component is normalized using min-max scaling:
`normalized = (value - min) / (max - min)`

For CIR, normalization is reversed since lower is better:
`normalized = (max - value) / (max - min)`

**Weights (conservative investor profile):**
| Dimension | Metric | Weight |
|---|---|---|
| Profitability | ROA 2024 | 32.5% |
| Stability | Equity to Assets 2024 | 32.5% |
| Efficiency | CIR 2024 | 20.0% |
| Growth | Asset Growth | 15.0% |

## Known limitations
- End-of-period assets and equity used for ROA/ROE denominators, not period averages
- NPL ratios excluded due to inconsistent disclosure format across banks
- Quarterly breakdowns excluded — annual data only
- Composite score weights reflect a conservative investor profile; weights are subjective
