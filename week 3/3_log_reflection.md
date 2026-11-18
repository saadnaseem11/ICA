# Week 3 – Log and reflection

**Prompt I used:**
> Here is a table of weekly prices for four items over 12 weeks (1 Jan – 19 Mar 2026) in two cities, PKR per kg. These are invented teaching data. Interpret it: what does it tell us about prices?
>
> | Item | n | Mean | Median | Min | Max | First | Last | % change |
> |---|---|---|---|---|---|---|---|---|
> | Oil B | 24 | 324.8 | 324.0 | 298.0 | 350.0 | 301.0 | 347.0 | 15.3 |
> | Pulse C | 23 | 205.9 | 206.0 | 200.0 | 213.5 | 200.0 | 207.5 | 3.8 |
> | Staple A | 23 | 111.3 | 112.5 | 99.5 | 122.0 | 104.0 | 117.5 | 13.0 |
> | Sweetener D | 23 | 167.2 | 167.5 | 149.0 | 184.5 | 152.0 | 181.5 | 19.4 |

**AI response:** 
*Across the 12 weeks from 1 January to 19 March 2026,
1.🟢 **all four items ended more expensive than they began**. 
2.🟠These invented figures suggest a broad upward price trend across the two cities.

3..- 🟢**Sweetener D** had the largest increase: **19.4%**, from PKR 152.0 to 181.5 per kg.
4.🟢 It also had the widest price range, from 149.0 to 184.5.
5.- 🟢**Oil B** rose **15.3%**, from PKR 301.0 to 347.0 per kg. 
6.🟢It was the most expensive item on average, at PKR 324.8.
7.- 🟢**Staple A** rose **13.0%**, from PKR 104.0 to 117.5 per kg.
8.v-🟢 **Pulse C** changed least, rising **3.8%**, from PKR 200.0 to 207.5. 
9. 🟠Its smaller min-to-max range suggests the steadiest prices of the four.

10.🟠The means and medians are close for each item, so the averages do not appear to be driven by a few unusually high or low observations.
11.🟢 Still, the table gives only summary statistics: it doesn’t show whether prices rose steadily, when they fluctuated, or how the two cities differed. 
12.🟢The observation counts also vary slightly (23 or 24), so the summaries may not be based on exactly the same number of records for every item.)*


Colour key: 🟢 can recompute · 🟠 explanation · 🔴 causal claim, or refers to data I wasn't shown

| # | AI claim | Colour | How I checked | Verdict |
|---|---|---|---|---|
| 1 | All four items ended more expensive than they began | 🟢 | Stats table: last > first for every item (Oil B 347 > 301, Pulse C 207.5 > 200, Staple A 117.5 > 104, Sweetener D 181.5 > 152) | Accepted |
| 2 | The figures suggest a broad upward price trend across the two cities | 🟠 | The table only shows first and last week, so it can't show a trend. Weekly table in notebook: Oil B rises every week; Staple A and Sweetener D rise with small dips; Pulse C zig-zags between nearby values | Partly accepted: true for Oil B, Staple A, Sweetener D; not for Pulse C |
| 3 | Sweetener D had the largest increase, 19.4%, from 152.0 to 181.5 | 🟢 | (181.5 − 152) ÷ 152 × 100 = 19.41%. Largest value in pct_change column | Accepted |
| 4 | Sweetener D had the widest price range, 149.0 to 184.5 | 🟢 | Range = max − min: Oil B 52.0, Sweetener D 35.5, Staple A 22.5, Pulse C 13.5 | Rejected: Oil B has the widest range (52.0); Sweetener D is second |
| 5 | Oil B rose 15.3%, from 301.0 to 347.0 | 🟢 | (347 − 301) ÷ 301 × 100 = 15.28% | Accepted |
| 6 | Oil B was the most expensive on average, at 324.8 | 🟢 | Mean column: Oil B 324.8 > Pulse C 205.9 > Sweetener D 167.2 > Staple A 111.3 | Accepted |
| 7 | Staple A rose 13.0%, from 104.0 to 117.5 | 🟢 | (117.5 − 104) ÷ 104 × 100 = 12.98% | Accepted |
| 8 | Pulse C changed least, rising 3.8%, from 200.0 to 207.5 | 🟢 | (207.5 − 200) ÷ 200 × 100 = 3.75%. But per-city table shows City 2 is missing on 1 Jan, so this is City 1 only. "Start week" cell: moving the start or end by one week gives 1.2% to 3.8% | Accepted, with caveat: City 1 only and sensitive to which weeks are compared |
| 9 | Pulse C's smaller min-to-max range suggests the steadiest prices | 🟠 | Smallest range (13.5) and smallest sd (3.91 vs 6.27–14.53). But weekly table shows it moves up and down every week rather than staying fixed | Accepted as a possible interpretation: steadiest level, not unchanging |
| 10 | Means and medians are close, so averages aren't driven by unusual observations | 🟠 | mean − median gaps: Oil B +0.83, Pulse C −0.09, Staple A −1.24, Sweetener D −0.35, all under 1.3. Part 2: this only holds after cleaning; with the 9999 left in, Sweetener D's mean was 576.81 vs median 167.75 | Accepted for the cleaned data only |
| 11 | The table shows only summary statistics, not whether prices rose steadily, fluctuated, or differed by city | 🟢 | Checked the table I gave: no weekly or per-city columns. This contradicts the AI's own "trend" claim in row 2 | Accepted |
| 12 | Observation counts vary slightly (23 or 24) | 🟢 | n column: Oil B 24, others 23. Cause: 3 prices missing and flagged in my Week 2 cleaning (Pulse C City 2 1 Jan, Staple A City 2 15 Jan, Sweetener D City 1 22 Jan) | Accepted |


##  Confused Classmate (excerpt)

**Prompt I used:**
> Play a classmate in my statistics class who firmly believes "the mean is always the typical price". Don't give in easily. After each of my explanations, ask "but why?" or raise a new objection. Only stop when you're genuinely convinced. Keep each turn short.

**Excerpt:** *(paste 6–10 turns: yours and the AI's)*

Me:The mean is always the typical price

Classmate: Exactly. The mean uses every price, so it has to be the most representative one. Why would the median be better?

Me: Using every price is exactly the problem. The mean adds everything up and divides, so one huge price pulls it up. In my data, Sweetener D’s prices are all between 149 and 184.5. One wrong entry of 9999 makes the mean 577, and no shop ever charged that.

Classmate: But why call 577 untypical? It’s still the balance point of all the entries. Maybe 9999 is a data error, and correcting it would make the mean typical again.

Me:Typical means close to what most prices look like. All 23 real prices are between 149 and 184.5. 577 is far from every one of them, while 167.75 sits right in the middle of them.

Classmate: But why should “typical” mean close to most observations? The mean summarizes the whole dataset, including unusual values. Couldn’t you say 577 is typical of the data as recorded, even if it’s a poor description of the usual shop price?

Me:typical is a claim about what a price usually looks like, and not a single recorded price is anywhere near 577. Also, 9999 isn’t a price at all. It’s a code for a missing value. So 577 accurately summarises a mistake. That’s why “typical” should mean close to most observations: it has to describe the prices, not the errors.

Classmate:Okay, if 9999 is a missing-value code, it shouldn’t be included as a price. I’m convinced for this dataset: the mean is not always the typical price. The claim that the mean is “always” typical doesn’t hold when an invalid entry pulls it far from all the actual prices.


**Explanation I used** (my own words):
- The mean is the total divided by the count. Every value pulls on it in proportion to its size, so one huge or tiny value drags it.
- The median is the middle value when prices are sorted. A huge value just becomes "the last one in the list", so the middle barely moves.
- In my data: Sweetener D's prices are all between 149 and 184.5. Add one 9999 and the mean becomes 577, a price no shop ever charged. The median goes from 167.50 to 167.75.
- "Typical" should mean a value close to what most observations look like. 577 is not close to any of them; 167.75 is.
- When there are no extreme values (my cleaned data), mean and median are almost the same, so the mean *is* typical then. It isn't *always* typical.
- Neither one tells you whether the price went up. For that, compare the same city on two dates.

## Reflection: where did my first draft say more than the data allowed?

1. **The C sentence.** "Rising costs pushed up the prices" is a causal claim. The file has prices, dates and cities only: no costs, wages, fuel or anything else that could show a cause. The most the data support is the O sentence that prices rose, plus a clearly labelled possible explanation.
2. **The word "staple".** The note risks sounding like a statement about real prices in Pakistan. The data are illustrative teaching figures, so the note can only describe this file.
3. **Pulse C.** My first instinct was a single "+3.8%". The weekly table showed that number depends on starting on a low week. Changing either endpoint by one week gives +1.2% to +3.8%. A range is the honest report.
4. **The E sentence about the neighbours.** I don't know what data they used. It is labelled as a possible explanation, and it has to stay that way.
5. **Compared with the AI.** My draft made a causal claim (red); the AI made none. But the AI called the change a "trend" from a table that only showed two dates (row 2), and it got one checkable fact wrong (row 4: Oil B, not Sweetener D, has the widest range). Its numbers looked careful, but I only found the error by recomputing every one.