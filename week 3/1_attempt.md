# Week 3 – Attempt 1 (before AI)

**Data:** my Week 2 cleaned file (`teaching_prices_clean_week2.csv`): 96 rows, 4 items × 2 cities × 12 weeks (1 Jan – 19 Mar 2026). Three prices are missing and flagged (Pulse C City 2 on 1 Jan, Staple A City 2 on 15 Jan, Sweetener D City 1 on 22 Jan). Illustrative teaching data, not actual PBS observations.

## 1. Statistics per item (PKR per kg)

| Item | n | Mean | Median | Mean − median | First → last (same cities) | % change |
|---|---|---|---|---|---|---|
| Oil B | 24 | 324.83 | 324.00 | +0.83 | 301.0 → 347.0 | +15.3% |
| Pulse C | 23 | 205.91 | 206.00 | −0.09 | 200.0 → 207.5 (City 1 only) | +3.8% |
| Staple A | 23 | 111.26 | 112.50 | −1.24 | 104.0 → 117.5 | +13.0% |
| Sweetener D | 23 | 167.15 | 167.50 | −0.35 | 152.0 → 181.5 | +19.4% |

First → last = average of City 1 and City 2 on 1 Jan vs 19 Mar. Pulse C has no City 2 price on 1 Jan, so I used City 1 at both ends. Averaging "whatever is there" would compare City 1 alone with the two-city average and give +5.25%, which mixes up a city difference with a price change.

## 2. Which statistic I would report, and why

- **Oil B:** % change (+15.3%). The price rises almost every week. Mean and median are nearly equal, but both describe the average level over the quarter, not whether the price rose.
- **Staple A:** % change (+13.0%), median 112.5 if a "typical price" is needed. The rise is steady. The median is a safer level here because one week (City 2, 15 Jan) is missing.
- **Sweetener D:** % change (+19.4%). It has the clearest steady rise. Mean and median differ by only 0.35 after cleaning.
- **Pulse C:** median (206) with the % change given as a range. The price alternates between nearby values (200 / 202.5 / 205 in City 1), so first-to-last depends on which weeks you pick: +1.2% to +3.8%. One % figure would sound more precise than the data allow.

## 3. With and without a flagged value (Week 2 file, Sweetener D)

| | With 9999 | Without 9999 (my Week 2 decision) | Difference |
|---|---|---|---|
| n | 24 | 23 | 1 |
| Mean | 576.81 | 167.15 | +409.66 |
| Median | 167.75 | 167.50 | +0.25 |

**Explanation:** the mean adds up every value, so one entry of 9999 (about 60 times the usual price) pulls the mean to 577, higher than any real price in the series. The median only depends on the middle of the sorted values. Adding one huge number moves the middle by half a position, so it shifts by just 0.25. The same thing happens with Staple A's "1,250": the mean goes from 111.26 to 158.71 while the median stays at 112.50.

## 4. Draft referee's note (labelled)

> **Referee's note: who's right about the staple prices?**
>
> **O** Across two cities over 12 weeks (1 Jan – 19 Mar 2026), each item’s mean and median prices are less than 1.3 rupees per kg apart; Oil B’s mean is 324.8 and its median is 324.0.
> **O** So, with this cleaned data, using the mean or median gives much the same result.
> **O** Neither statistic shows whether prices rose, since each summarises the entire quarter.
> **O** Comparing the first and last weeks in the same cities, Sweetener D increased by about 19%, Oil B by about 15% and Staple A by about 13%.
> **O** Pulse C changed very little: it rose by between 1% and 4%, depending on the weeks compared, as its price fluctuates by a couple of rupees from week to week.
> **O** The two measures differ substantially only when there’s an error in the data: a mistyped Sweetener D price of 9999 would push its mean to 577 rupees, while its median would remain near 167.
> **E** *Possible explanation:* the neighbours could be looking at different versions of the figures—one with an error like this—or comparing different weeks.
> **C** Higher costs caused the prices of Sweetener D, Oil B and Staple A to rise.
> **O** To resolve the disagreement fairly, compare the price in the same city on two dates, and use the median when asking for a “typical price.”
> **O** These figures are for teaching purposes; they illustrate prices in two cities and are not official observations.
