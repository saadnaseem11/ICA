‘3_log_reflection.md’

# AI Log & Reflection

### What i asked AI:

What is unclear in these questions? What data would I need? What might I be assuming?

### What AI suggested:

“Items” is undefined. Which items? A fixed basket tracked over time, everything a store sells, or whatever happens to appear in the data? If items enter and leave the dataset, “most items” may only describe the survivors.
“Price” is ambiguous. Sticker price, price per unit, price after promotions, or price including tax? Shrinkflation (smaller package, same price) would make prices look flat while costs rise.
The endpoints are fragile. Using only the earliest and latest dates ignores everything in between. A sale, a holiday, or a one-off spike on either end can distort the result.
No adjustment for inflation or income. “Higher price” in nominal terms isn’t the same as “costs more” in real terms or relative to what people earn.
Question 1 has no threshold. A 0.1% increase counts as “higher,” which isn’t what most people mean by “everything costs more.”
Question 2 uses 5%, but over what period? 5% over one year is very different from 5% over ten. The threshold should scale with the time span.
“Most” is vague. More than 50%? 75%? And “most” counts items equally, though a price change in rent matters more than one in paper clips.
Neither question tests the actual claims. Claim 1 is about cost, Claim 2 is about spending behavior. Price data alone speaks to neither fully.
The claims aren’t opposites. Both could be partly true: prices rise and people shift spending.
What data you’d need
* Prices for the same items at multiple points in time, not just two
* Clear item definitions: brand, size, unit, category
* Quantity or sales data, to see what people buy and whether that changed
* Weights, such as share of the average household budget, so important items count more
* A consistent source, store or region, so you’re not comparing different markets
* A general inflation index (like CPI) as a benchmark
* Income or wage data, for affordability
* Promotions or discount flags
* For Claim 2 especially: spending by category over time, and substitution data (e.g., switching from name brand to store brand)
What you might be assuming
* The same items exist at both dates and are truly comparable
* Two dates are representative of the whole period
* A price rise means a cost-of-living rise, ignoring wages, quality, and package size
* Every item matters equally
* “Spend differently” can be seen in price data alone
* Seasonality isn’t a factor (comparing January to July for produce, for example)
* The data is a fair sample rather than skewed toward certain stores or goods
* The 5% cutoff has meaning rather than being arbitrary


### Five Alternative questions:

Among items present at every date, what share rose by more than the overall inflation rate?

What is the median annual price change per item?  Weighted by typical household spending, how much did the cost of basket change between the start and end of the period?

Did the share of total spending going to each category change, and did people move toward cheaper substitutes as prices rose?

Did prices grow faster or slower than wages over the same period, so items became relatively more or less affordable?

### What I learned:

1. A good question is specific
2. Every question rests on assumptions.
3. Data can only answer some questions.
4. AI output is a list of suggestions, not answers.
5. I make the final decisions
