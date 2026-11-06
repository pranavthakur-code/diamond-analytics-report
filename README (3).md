# Diamond Inventory Analytics Report

Business analytics project: where is the value in a diamond inventory, and what should a
category manager do about it? (Scenario created for an internship assignment.)

**Data:** 53,940 diamond listings (ggplot2 `diamonds`, via
[seaborn-data](https://github.com/mwaskom/seaborn-data/blob/master/diamonds.csv)). Historical listing prices in USD, not sales.

## Headline results
- Stones of 1 carat or more are 35% of listings but 73% of listed value.
- A 10% larger stone costs about 20% more; carat, cut, colour and clarity explain 98% of price variation.
- Ideal cut has the lowest average price only because the stones are smaller; per carat in the 1.0-1.49 band it earns 40% more than Fair.
- Pricing cliff at 1.00 carat: 1,546 listings at 1.00 ct vs 23 at 0.99 ct, with about 18% higher price per carat.

## Recommendations (summary)
1. Prioritise buying and stock availability for 1 ct and above.
2. A/B test a "near-one-carat" range of 0.90-0.99 ct.
3. Report price per carat within carat bands instead of average price.
4. Position Ideal/Premium as quality tiers; use clarity as the main quality lever in range planning.

## Files
| File | Description |
|---|---|
| `Diamond_Analytics.ipynb` | Executed notebook: cleaning, KPIs, analysis, charts |
| `diamonds.csv` | Dataset |
| `fig*.png` | Dashboard and chart exports |

## Run it
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
jupyter notebook Diamond_Analytics.ipynb
```
Keep `diamonds.csv` in the same folder as the notebook.

## Limitations
Listing prices only (no sales, costs or margins); historical snapshot; regression shows association, not causation.
