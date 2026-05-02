# 🏦 Kyrgyzstan Banking Sector — Financial Analysis 2024

> End-to-end solo portfolio project: financial analysis of 13 Kyrgyzstan 
> commercial banks built from raw IFRS annual report PDFs to a 
> published Power BI dashboard.

![Profitability Quadrant](Dashboard/Screenshots/Profitability.png)

## 🎯 Project goal

Analyze and compare the 2024 financial performance of all major commercial 
banks in Kyrgyzstan using publicly available IFRS annual reports, and surface 
actionable insights for investors and depositors.

## 🔑 Key findings

**Profitability:** Keremet Bank leads the sector with an ROA of 8.48%, 
followed by MBANK at 8.00%. Both improved year-over-year, while Demir Bank 
and Doscredo Bank saw notable ROA declines — signaling that assets grew 
faster than profits, an efficiency warning worth monitoring.

**Growth:** MBANK was the most aggressive expander in 2024, growing total 
assets by 67.18% and loans by 49.44%. However, its equity-to-assets ratio 
of 16.25% — near the sector bottom — raises the question of whether rapid 
asset expansion can be sustained without a proportional increase in its 
capital buffer.

**Stability:** Keremet Bank holds the strongest capital position in the 
sector at 39.90% equity-to-assets, nearly double the second-placed Capital 
Bank at 20.73%. For a depositor, this means Keremet Bank has the largest 
capital buffer to absorb potential losses before depositor funds are at risk.

**Efficiency:** MBANK operates at a cost-to-income ratio of 28.50% — 
exceptionally lean by any benchmark. For every 100 KGS of operating income 
generated, only 28.50 KGS is spent on running the bank.

**Vulnerability signals:** KKB is the only bank that contracted across all 
three growth metrics simultaneously — assets shrank by 5.78%, loan portfolio 
by 17.79%, and net profit growth was the lowest in the sector. Doscredo Bank 
showed similar deterioration — net profit fell 37.06% year-over-year while 
its cost-to-income ratio worsened from 73.30% to 83.51%.

**Composite ranking:** Using a weighted scoring model (profitability 32.5%, 
stability 32.5%, efficiency 20%, growth 15%), Keremet Bank and MBANK emerge 
as the top two banks for conservative investors — strong on fundamentals 
across all dimensions simultaneously.

## 🏦 Banks analyzed

13 commercial banks: Aiyl Bank, Bai Tushum, Bakai Bank, Capital Bank, 
Companion Bank, Demir Bank, DosCredoBank, Eldik Bank, KICB, 
Kyrgyzkommertsbank, Keremet Bank, MBANK, Optima Bank.

## 📊 Dashboard

Download `dashboard/kyrgyzstan-banks-2024-long.pbix` and open in 
Power BI Desktop to explore the interactive version.

### Dashboard pages
- **Profitability** — ROA vs ROE quadrant chart with bubble size = assets
- **Growth** — year-over-year growth across assets, loans, and profit
- **Stability** — capital strength and cost efficiency comparison
- **Rankings** — composite score ranking with conditional formatting

## 🛠 Tech stack

Power BI Desktop · DAX · Power Query (M) · Excel

## 📁 Repository structure
kyrgyzstan-banks-2024/
├── dashboard/
│   ├── kyrgyzstan-banks-2024-long.pbix
│   └── screenshots/
├── data/
│   ├── raw/                    # 13 bank annual report PDFs
│   └── processed/
│       └── banks_2024.xlsx
├── docs/
│   ├── scope.md
│   ├── methodology.md
│   └── data-dictionary.md
└── information/                # Original project brief

## ▶️ How to reproduce

1. Clone: `git clone https://github.com/MSultanbek/kyrgyzstan-banks-2024.git`
2. Open `dashboard/kyrgyzstan-banks-2024-long.pbix` in Power BI Desktop
3. Data source points to `data/processed/banks_2024.xlsx` — click Refresh
4. Metric calculations documented in `docs/methodology.md`

## 📬 Contact

Sultanbek Muratbekov · sultanbek.muratbekov@alatoo.edu.kg ·
[GitHub](https://github.com/MSultanbek)