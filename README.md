# India-Stocks-2161-2190-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2161 to 2190)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2161-2190-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2161 to 2190)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2161 | `SHANTI` | Shanti Overseas (India) Limited | `SHANTI.NS` |
| 2162 | `SHANTIGEAR` | Shanthi Gears Limited | `SHANTIGEAR.NS` |
| 2163 | `SHANTIGOLD` | Shanti Gold International Limited | `SHANTIGOLD.NS` |
| 2164 | `SHARDACROP` | Sharda Cropchem Limited | `SHARDACROP.NS` |
| 2165 | `SHARDAMOTR` | Sharda Motor Industries Limited | `SHARDAMOTR.NS` |
| 2166 | `SHARDUL` | Shardul Securities Limited | `SHARDUL.NS` |
| 2167 | `SHAREINDIA` | Share India Securities Limited | `SHAREINDIA.NS` |
| 2168 | `SHBAJRG` | Shri Bajrang Alliance Limited | `SHBAJRG.NS` |
| 2169 | `SHEKHAWATI` | Shekhawati Industries Limited | `SHEKHAWATI.NS` |
| 2170 | `SHEMAROO` | Shemaroo Entertainment Limited | `SHEMAROO.NS` |
| 2171 | `SHERVANI` | Shervani Industrial Syndicate Limited | `SHERVANI.NS` |
| 2172 | `SHILCTECH` | Shilchar Technologies Limited | `SHILCTECH.NS` |
| 2173 | `SHILGRAVQ` | Shilp Gravures Limited | `SHILGRAVQ.NS` |
| 2174 | `SHILPAMED` | Shilpa Medicare Limited | `SHILPAMED.NS` |
| 2175 | `SHINDL` | Sharat Industries Limited | `SHINDL.NS` |
| 2176 | `SHIPROCKET` | Shiprocket Limited | `SHIPROCKET.NS` |
| 2177 | `SHIVAAGRO` | Shiva Global Agro Industries Limited | `SHIVAAGRO.NS` |
| 2178 | `SHIVACEM` | Shiva Cement Limited | `SHIVACEM.NS` |
| 2179 | `SHIVALIK` | Shivalik Rasayan Limited | `SHIVALIK.NS` |
| 2180 | `SHIVAM-RE1` | Shivam Autotech Ltd-RE | `SHIVAM-RE1.NS` |
| 2181 | `SHIVAMAUTO` | Shivam Autotech Limited | `SHIVAMAUTO.NS` |
| 2182 | `SHIVAMILLS` | Shiva Mills Limited | `SHIVAMILLS.NS` |
| 2183 | `SHIVATEX` | Shiva Texyarn Limited | `SHIVATEX.NS` |
| 2184 | `SHIVAUM` | Shiv Aum Steels Limited | `SHIVAUM.NS` |
| 2185 | `SHK` | S H Kelkar and Company Limited | `SHK.NS` |
| 2186 | `SHOPERSTOP` | Shoppers Stop Limited | `SHOPERSTOP.NS` |
| 2187 | `SHRADDHA` | Shraddha Prime Projects Limited | `SHRADDHA.NS` |
| 2188 | `SHRADHA` | Shradha Realty Limited | `SHRADHA.NS` |
| 2189 | `SHREDIGCEM` | Shree Digvijay Cement Co.Ltd | `SHREDIGCEM.NS` |
| 2190 | `SHREEJISPG` | Shreeji Shipping Global Limited | `SHREEJISPG.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SHANTI 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2161-2190-Historical-Data/main/SHANTI/1m/2026/10/SHANTI_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
