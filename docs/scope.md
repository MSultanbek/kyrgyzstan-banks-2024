# Project Scope — Kyrgyzstan Banking Analysis 2024

## Primary audience
Investors looking for the banks to invest

## Business questions
1. Who is best at making money relative to their size?
2. Which banks have grown most in 2024?
3. Which banks are going to be eaten by other larger banks?
4. How does each bank's cost efficiency compare?
5. Which banks offer the strongest stability for depositors and creditors?

## Banks in scope

1. AB — Aiyl Bank (Айыл Банк)
2. Bai Tushum — Bank Bai-Tushum (Бай-Түшүм)
3. Bakai Bank — Bakai Bank (Бакай Банк)
4. Capital Bank — Capital Bank (Капитал Банк)
5. Companion Bank — Kompanion Bank (Банк Компаньон)
6. Demir Bank — Demir Kyrgyz International Bank (Демир Банк)
7. Doscredo Bank — Dos-Credobank (Дос-Кредобанк)
8. Eldik Bank — Eldik Bank (Элдик Банк, formerly known as RSK Bank)
9. KICB — Kyrgyz Investment and Credit Bank (Кыргыз Инвестициялык Кредит Банкы)
10. KKB — Kyrgyzkommertsbank (Кыргызкоммерцбанк)
11. Keremet Bank — Keremet Bank (Керемет Банк)
12. MBANK — MBANK (Commercial Bank Kyrgyzstan)
13. Optima Bank — Optima Bank (Оптима Банк)

## Metrics to collect (raw)
- net profit
- total assets
- equity
- loans
- deposits
- operating expenses
- operating income
- total liabilities
- interest income
- interest expense 
- net interest income = interest income − interest expense

## Metrics to derive (calculated)
- ROA = net profit / total assets
- ROE = net profit / equity
- Cost-to-Income Ratio (CIR) = operating expenses / operating income
- YoY growth rate for: assets, loans, deposits, net profit
- Equity-to-assets ratio = equity / total assets

## Out of scope
**Quarterly breakdowns** — a deeper analysis would track each bank quarter-by-quarter through 2024. I'm excluding this because not all banks publish quarterly reports in accessible format, and annual data is sufficient to answer my five questions.

**NPL ratios (non-performing loans)** — this would strengthen question 3 significantly. I'm excluding it because NPL disclosure format varies across banks and reliable extraction would require a separate data collection effort.

**NBKR sector benchmark comparison** — comparing each bank against national sector averages would add context. Excluding for now; worth adding in a future version

## Deliverables
- [ ] Consolidated dataset (banks_2024.csv)
- [ ] Power BI dashboard (.pbix)
- [ ] Executive summary (docs/executive-summary.pdf)
- [ ] Professional README