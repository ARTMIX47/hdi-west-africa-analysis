# Human Development Trends in West Africa and Rwanda, 1990–2023

An exploratory analysis of the Human Development Index (HDI) and its components for 11 countries, using open data from the United Nations Development Programme (UNDP).

## Objective

To understand how human development has evolved across countries with very different trajectories, and to identify what drives differences in HDI: health, education or income.

## Countries analysed

Benin, Cabo Verde, Côte d'Ivoire, Ghana, Mali, Niger, Nigeria, Rwanda, Senegal, Sierra Leone, Togo.

The sample was chosen for contrast (stable countries, fast improvers, post-conflict contexts and low-HDI countries), not to be statistically representative of the region.

## Data

- **Source:** UNDP Human Development Report Office, *Human Development Report 2025*, composite indices complete time series (1990–2023).
- **File:** `HDR25_Composite_indices_complete_time_series.csv`
- **Download:** https://hdr.undp.org/data-center/documentation-and-downloads
- **Variables used:** HDI, life expectancy at birth, mean years of schooling, GNI per capita (PPP$).

## Methods

1. Loaded the UNDP CSV with Python (pandas) and filtered the 11 countries by ISO3 code.
2. Reshaped the data from wide to long format and checked missing values.
3. Computed HDI gains per country. Rwanda has no data before 1995 and Cabo Verde before 2000, so **all cross-country comparisons use the same period, 2000–2023**.
4. Compared the 2023 components (health, education, income) across countries.
5. Visualised results with matplotlib.

Tools: Python, pandas, matplotlib, Google Colab.

## Key findings

**1. Every country improved, but at very different speeds.**
Over 2000–2023, Rwanda recorded by far the largest HDI gain (+0.238, from 0.340 to 0.578), followed by Côte d'Ivoire (+0.163) and Niger (+0.153). The smallest gains were in Cabo Verde (+0.083), Mali (+0.099) and Benin (+0.100).

**2. Low-HDI countries are catching up, but gaps remain large.**
Niger gained +0.153 since 2000 (from 0.266), yet Niger and Mali both stand at 0.419 in 2023, the lowest in the sample. Cabo Verde has the highest HDI (0.668) despite the smallest gain, because it started from the highest level (0.585 in 2000).

**3. Income alone does not explain human development.**
Rwanda (GNI per capita of about $2,971) and Togo (about $2,856) reach HDI values of 0.578 and 0.571. This is higher than Nigeria (about $5,569; HDI 0.560), Senegal (about $4,202; HDI 0.530) and Benin (about $3,806; HDI 0.515), which have higher incomes.

**4. Countries face different bottlenecks.**
- Nigeria has the highest mean years of schooling in the sample (7.6 years) but the lowest life expectancy (54.5 years), which holds its HDI down.
- Senegal has the second-highest life expectancy (68.7 years) but only 2.9 mean years of schooling.
- Niger (1.4 years) and Mali (1.6 years) have the lowest schooling levels, which points to education as a key constraint.

## Limitations

- This is a descriptive analysis: it shows associations and does not establish causes.
- The HDI education dimension combines mean and expected years of schooling; only mean years of schooling was analysed here.
- With 11 selected countries, results should not be generalised to the whole region.
- HDI values come from the 2025 UNDP release and may be revised in future editions.

## How to reproduce

1. Open the notebook in Google Colab or Jupyter.
2. Run all cells. The data is loaded directly from the UNDP URL.

## Files

- `notebook.ipynb`: full analysis code
- `hdi_gain_2000_2023.png`: HDI gain by country, same period
- `income_vs_hdi.png`: income versus HDI, 2023

## Author

[Aumeric Dumor] · Computer Science · [aumericd@gmail.com]
