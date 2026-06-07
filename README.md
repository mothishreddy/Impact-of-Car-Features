# 🚗 Impact of Car Features — Project 2

📊 Data analysis project exploring how car features like engine power, fuel efficiency &amp; market segment impact automobile pricing and consumer demand.

---

## 📌 Project Overview

The automobile industry is evolving rapidly, with growing emphasis on fuel efficiency, environmental sustainability, and technological innovation. This project analyzes a dataset of over 11,000 automobile models to help automakers **optimize pricing and product decisions** to maximize profitability while meeting consumer demand.

**Core Question:**
> *"How can an automaker optimize pricing and product development to maximize profitability while meeting consumer demand?"*

---

## 📊 Dataset

| Property | Value |
|---|---|
| Total Observations | 11,159 |
| Variables | 16 |
| Records After Cleaning | 8,172 |
| Source | Edmunds.com automobile dataset |

### Key Variables
- `Make`, `Model`, `Year`
- `Fuel Type`
- `Engine HP`, `Engine Cylinders`
- `City MPG`, `Highway MPG`
- `Market Category` (Segment)
- `MSRP` (Price)
- `Popularity`

### Data Cleaning
- Missing values in **Number of Doors** filled logically
  - Sedans → assumed 4 doors
  - Coupes → assumed 2 doors
- Outliers retained for analysis
- Final clean dataset: **8,172 records**

---

## 🔍 Analytical Tasks

### Task 1 — Popularity Analysis
Explored differences in car popularity across market segments using pivot tables and combination charts.

**Key Findings:**
- Top segments by avg. popularity: **Crossover + Flex Fuel + Performance**, **Flex Fuel + Diesel**, **Hatchback + Flex Fuel** — all at 5,657 avg views
- Grand total average popularity: **1,499**
- Crossover segment alone averages **1,545 views**

---

### Task 2 — Engine Power vs Price Correlation
Plotted engine HP against MSRP using a scatter chart with trendline.

**Key Findings:**
- **Positive correlation confirmed** between engine power and price
- Models with 1,001 HP priced between **$1.5M – $2.1M**
- Higher horsepower consistently associated with higher MSRP

---

### Task 3 — Key Factors Influencing Car Pricing (Regression Analysis)
Used linear regression to identify which automobile features most significantly affect vehicle price.

**Regression Results (Adj. R² = 0.439, n = 8,172):**

| Feature | Coefficient | Significance |
|---|---|---|
| Engine HP | +$414 per HP | p < 0.001 ✅ |
| City MPG | +$542 per MPG | p < 0.001 ✅ |
| Number of Doors | −$4,709 per door | p < 0.001 ✅ |
| Highway MPG | +$58 | p = 0.66 ❌ (not significant) |
| Engine Cylinders | +$0.57 | p = 0.99 ❌ (not significant) |

> The model explains **~44% of the variance** in car pricing.

---

### Task 4 — Manufacturer Price Comparison
Identified price variations across different automobile manufacturers using pivot tables and bar charts.

**Pricing Tiers:**

| Tier | Brands | Avg Price |
|---|---|---|
| Ultra-Luxury | Bugatti, Maybach, Rolls-Royce | $1.76M / $546K / $351K |
| Performance | Ferrari, Lamborghini, McLaren | $238K / $332K / $240K |
| Mainstream | Toyota, Honda, Ford, Mazda | $31K / $27K / $33K / $23K |

> Overall average MSRP across all manufacturers: **~$50,043**

---

### Task 5 — Fuel Efficiency Trends Over Time
Analyzed how average highway MPG changed from 1990 to 2017.

**Key Findings:**
- Clear **upward trend** in fuel efficiency from 1990 to 2017
- Highest avg highway MPG: **28.86 MPG (2016)**
- Lowest avg highway MPG: **21.16 MPG (2007)**
- Overall average across all years: **27.07 MPG**
- Dip in 2002–2007 reflects market shift toward larger, less efficient vehicles

---

### Bonus — Cylinders vs Fuel Efficiency
Examined the relationship between engine cylinder count and highway MPG.

- **Correlation Coefficient: −0.590** (moderate negative relationship)
- More cylinders = lower fuel efficiency
- Electric/hybrid vehicles (0 cylinders): 80–100+ MPG
- 16-cylinder exotics: ~14 MPG highway

---

## 💡 Key Business Conclusions

1. **Engine Power = Premium Price** — Each additional HP adds ~$414 to MSRP; target high-HP segments for premium positioning
2. **Fuel Efficiency Commands a Premium** — Urban MPG adds ~$542 per unit; eco-friendly vehicles justify higher price points
3. **Market Segmentation Drives Popularity** — Crossover + Flex Fuel + Performance combos are the most viewed; focus marketing here
4. **Manufacturer Pricing is Polarized** — Ultra-luxury and volume segments require completely different strategies
5. **Fuel Economy is Improving** — Highway MPG grew from ~23.5 (1990) to 28.86 (2016); invest in fuel tech for long-term competitiveness

---

## 🛠️ Tools & Tech Stack

| Tool | Purpose |
|---|---|
| **Microsoft Excel 2021** | Data cleaning, pivot tables, regression analysis, charts |
| **Canva** | Presentation design and visual storytelling |

> No programming libraries were required — all analysis performed in Excel.

---

## 📁 Project Structure

```
impact-of-car-features/
│
├── data/
│   └── car_features_dataset.xlsx       # Raw + cleaned dataset
│
├── analysis/
│   ├── task1_popularity.xlsx           # Pivot tables & charts — popularity
│   ├── task2_engine_vs_price.xlsx      # Scatter plot — HP vs MSRP
│   ├── task3_regression.xlsx           # Linear regression output
│   ├── task4_manufacturer_price.xlsx   # Manufacturer price comparison
│   └── task5_fuel_efficiency.xlsx      # MPG trends over time
│
├── presentation/
│   └── Impact_of_Car_Features.pptx    # Final presentation deck (10 slides)
│
└── README.md
```

---

## 📈 Results Summary

```
Dataset        : 11,159 observations → 8,172 after cleaning
Model R²       : 0.439 (44% of price variance explained)
Top Price Driver  : Engine HP (+$414/HP)
Top Segment       : Crossover + Flex Fuel + Performance (5,657 avg views)
Avg Market Price  : ~$50,043
Peak Fuel Economy : 28.86 MPG highway (2016)
```

---

## 👤 Author

**Mothish R**  
Project — 2 | Data Analysis

---

## 📄 License

This project is for academic and educational purposes only.
