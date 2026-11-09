# Commercial Banks' Reliability Assessment (Ukraine, 2018–2023)

Bachelor thesis, Kyiv National Economic University (2023).
Language: R. 

## Goal
Assess, rank, and forecast the reliability of Ukrainian commercial banks using
economic-mathematical modelling, including the effect of the 2022 war.

## Data
Financial indicators of 67 Ukrainian banks (state-owned, private, and with
foreign capital), 1 January 2018 – 1 January 2023. Source: National Bank of Ukraine.

## Methods
1. **Reliability rating** built from six indicators: absolute liquidity ratio,
   capital adequacy, deposit-to-loan ratio, return on assets (ROA), return on
   equity (ROE) and coverage ratio.
2. **Cluster analysis** (k-means and hierarchical) of banks for 2021 and 2022 into three groups:
   low, medium and high reliability.
3. **Time-series forecasting** of each bank's rating. Compared ARIMA, ETS and
   STL-based models; ARIMA gave the most accurate forecasts (lowest RMSE).

## Key findings

**Effect of the war.** Reliability indicators fell for many banks after the
start of the war, but by January 2023 nearly all banks were returning to normal
levels, and none dropped to critical levels. For banks with state or foreign
capital, the rating fell by almost half after the outbreak of the war.

![Figure 1](https://github.com/user-attachments/assets/c57175b0-1ab1-4ba1-a477-757911c0c38b)
![Figure 2](https://github.com/user-attachments/assets/c3c520c6-a2fa-426a-bf87-c81c4d10fd01)
![Figure 3](https://github.com/user-attachments/assets/7d1a18fe-8d94-4f65-93a1-18c856dda93e)

**Outliers.** Ratings of state-owned banks follow an approximately normal
distribution, while private and foreign banks show many outliers (e.g. JSC BANK
AVANGARD and JSC BTA BANK, with ratings of 58–233 against a normal maximum of 7).
The rating correlates strongly with the deposit-to-loan ratio, which explains
these extreme values. Capital adequacy is related to the coverage ratio, and ROA
to ROE.

![Figure 4](https://github.com/user-attachments/assets/1485821e-15ef-4d8e-b019-9131329ce407)

**Ranking by ownership.** Among state-owned banks, PrivatBank led in 2021 (7.08)
and Oschadbank in 2022 (4.14), after PrivatBank moved to the outlier cluster.
Private banks were the most stable after the invasion; BANK PORTAL led in both
years and increased its rating.

![Figure 5](https://github.com/user-attachments/assets/d8082f53-e40d-4e3c-ac4e-d8002df30ad1)

**Clustering.** Banks split into three groups. The 2022 clustering separated the
groups more clearly, and many banks had negative ROA and ROE that year. Average
rating by cluster, 2021 → 2022:

| Cluster | 2021 | 2022 |
|---|---|---|
| High reliability | 5.51 | 5.85 |
| Medium reliability | 3.89 | 3.76 |
| Low reliability | 3.03 | 2.36 |

The low-reliability group was affected by the war most. It includes e.g.
JSC Ukrsimbank, JSC BANK FORWARD and JSC Sens Bank; the high-reliability group
includes e.g. JSC CB PrivatBank, JSC Concorde Bank and JSC Altbank.

![Figure 6](https://github.com/user-attachments/assets/8d4d2474-2161-4e6e-be68-4a75ebfa22b7)
![Figure 7](https://github.com/user-attachments/assets/5904c336-e1b9-44da-9f48-46e19ca7b472)
![Figure 8](https://github.com/user-attachments/assets/a9c44a21-e2b9-4ca7-a476-5b9dcfcade83)
![Figure 9](https://github.com/user-attachments/assets/550b1e4b-a542-4d01-be93-50ee97ecf099)
![Figure 10](https://github.com/user-attachments/assets/abdafcc1-ba1f-46ff-be81-04a340795bbf)
![Figure 11](https://github.com/user-attachments/assets/cd09e64e-f823-43a2-a2fa-60d84571c793)

**Forecasts (ARIMA).** For example, the forecast shows JSCB "Lviv" rising only
slowly, Raiffeisen Bank declining until April 2024 and then stabilising, and
PrivatBank staying at a high level.

## Limitations
- The rating is driven partly by the deposit-to-loan ratio, which causes
  extreme values for some banks; results should be read as a relative ranking.
- Forecasts are model-based, with no external validation after 2023.
