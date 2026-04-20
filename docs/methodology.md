# Methodology — Kyrgyzstan Banking Analysis 2024

## Units
All monetary values are in **millions of KGS**.
Banks reporting in thousands were divided by 1,000 during extraction.

## Statements used per bank
| Bank | PDF file | Statements used |
|---|---|---|
| Aiyl Bank | AB.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Bai Tushum | Bai_Tushum.pdf | Statement of Financial Position, Statement of Comprehensive Income |
| Bakai Bank | Bakai Bank.pdf | |
| Capital Bank | Capital Bank.pdf | |
| Companion Bank | Companion Bank.pdf | |
| Demir Bank | Demir Bank.pdf | |
| Doscredo Bank | Doscredo Bank.pdf | |
| Eldik Bank | Eldik Bank.pdf | |
| KICB | KICB.pdf | |
| KKB | KKB.pdf | |
| Keremet Bank | Keremet Bank.pdf | |
| MBANK | MBANK.pdf | |
| Optima Bank | Optima-Bank.pdf | |

## Derived metrics
| Metric | Formula |
|---|---|
| ROA | net_profit / total_assets |
| ROE | net_profit / equity |
| CIR | ABS(operating_expenses) / operating_income |
| Equity-to-Assets | equity / total_assets |
| YoY Growth | (value_2024 - value_2023) / value_2023 |

## Known limitations
- End-of-period assets used for ROA/ROE denominators, not period averages
- NPL ratios excluded due to inconsistent disclosure format across banks
- Quarterly breakdowns excluded — annual data only