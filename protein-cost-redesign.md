| [home page](https://aadgaonkar.github.io/aditi-adgaonkar-portfolio/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [protein cost redesign](protein-cost-redesign) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique by Design: How Much Does 30g of Protein Really Cost?

## Why I chose this visualization

For this assignment, I chose *How Much Does 30g of Protein Cost?*, an infographic by The Bodybuilding Dietitians (2021), featured in the February 2023 MakeoverMonday challenge. It compares ten common foods on the cost of getting the same 30 grams of protein and shows the corresponding calories. I liked the practical question behind it: a grocery shopper may want affordable protein, but package prices alone don't give a fair comparison.

The original graphic has a useful premise and recognizable foods. It also gave me a clear opportunity to redesign something that was already informative rather than just replace a chart for the sake of it. My goal was to make **cost and calories equally easy to compare**, without losing the original's simple ranking of protein sources.

**Original visualization:** [The Bodybuilding Dietitians, *What Are The Cheapest High-Protein Foods?* (November 26, 2021)](https://www.thebodybuildingdietitians.com/blog/how-cost-effective-is-your-high-protein-diet)

![Original infographic: How Much Does 30g of Protein Cost?](https://images.squarespace-cdn.com/content/v1/5d59f351fddabe00013cf3e6/f9b4b336-fe23-4260-aae3-19f6f8f72b8b/PROTEIN%2BCOST.png)

*Original infographic by The Bodybuilding Dietitians. The chart compares cost per 30 grams of protein, with calorie values written inside the bars. Prices were sourced from Woolworths Australia.*

## Step 1: Understanding the original

The chart uses vertical bars to compare the cost of obtaining 30 grams of protein from different foods, from chicken breast and whey protein isolate to salmon fillets and Quorn. Calories are supplied as labels within the cost bars. Its likely audience includes grocery shoppers, students, and people interested in fitness or eating more protein on a budget.

This is a **data-driven, declarative** chart in the *Good Charts* framework: it is making a particular comparison for readers rather than supporting open-ended analysis.

## Step 2: Critique using Stephen Few's Effectiveness Profile

I evaluated the chart using Stephen Few's Data Visualization Effectiveness Profile. The 1–10 ratings helped me separate what the chart communicates well from what could be improved.

| Criterion | Rating | My reasoning |
|---|---:|---|
| Usefulness | 8/10 | Comparing the cost of a common amount of protein is practical for grocery decisions, although prices vary by place and time. |
| Completeness | 6/10 | It includes food names, cost bars, and calories, but does not label every exact cost or explain the full calculation for each product. |
| Perceptibility | 6/10 | Relative costs are fairly easy to scan; comparing calorie numbers embedded inside the bars takes more effort. |
| Truthfulness | 7/10 | The 30g protein standard is consistent, and the retailer is named, but exact underlying product prices are not supplied with the chart. |
| Intuitiveness | 8/10 | The bar chart is familiar, although mixing calorie labels into the cost bars may imply a relationship not represented by bar height. |
| Aesthetics | 7/10 | Food pictures make the topic approachable but also add visual clutter, alongside angled product names. |
| Engagement | 7/10 | The everyday question and recognizable foods make the chart interesting, but the design does not invite easy comparison of both measures. |

### What worked and what didn't

The strongest design decision is to standardize every food to 30 grams of protein. That makes the comparison more meaningful than simply comparing prices per package. The original also ranks foods by cost and uses pictures to help identify products quickly.

My biggest criticism is that the chart introduces **two useful measures but visually prioritizes only one**. Bar heights encode cost, while calories appear as numbers inside those same bars. Readers can readily see the cost ranking, but they have to read and mentally compare each number to understand the calorie differences. The large food photographs and diagonal labels also make the graphic busier than it needs to be. Finally, the lack of exact cost labels and detailed calculation data limits reproducibility.

A lower cost for protein does not necessarily mean a food is nutritionally preferable: foods differ in other nutrients, convenience, and dietary suitability. The original article itself emphasizes eating a variety of protein sources.

### How this compares with *Good Charts*

Stephen Few's profile made me evaluate the visualization in a more structured way. Instead of relying on whether I liked the design, I considered usefulness, completeness, accuracy, clarity, intuitiveness, aesthetics, and engagement. *Good Charts*, by contrast, helped me ask what kind of communication this was and what the intended audience needed to understand. I found the two methods complementary: **Good Charts helped frame the purpose; Few helped identify weaknesses.**

One limitation of the effectiveness profile is that the rating categories overlap. Perceptibility and intuitiveness, for example, can be difficult to separate, and the scores still reflect my judgment. The framework also does not directly show whether a real viewer can complete a task successfully. This is why testing the proposed redesign was important.

## Step 3: Sketching a solution

I made a simple, hand-drawn-style wireframe instead of jumping straight into Tableau. I kept the same ten foods but proposed **two aligned horizontal bar charts**, with cost on the left and calories on the right. I planned to order the foods by cost so readers could compare the same row across the two measures.

![Simple hand-drawn-style wireframe for the protein cost redesign](protein-cost-wireframe.png)

*Wireframe concept, not a data-accurate chart. Bar lengths in the sketch are illustrative; the final bars use the reconstructed dataset.*

The sketch responded directly to the critique: horizontal names would be easier to read, separate bars would make both measures visually comparable, and the final chart would show numerical values with the appropriate units.

## Step 4: Testing with two people

I shared the wireframe with two students and asked what it showed, whether comparing cost and calories was straightforward, what felt confusing, and what they would change. These are summaries of the feedback rather than verbatim interview transcripts.

**Participant 1 (university student):** The participant understood that the design compared foods based on cost and calories and found the side-by-side layout easy to follow. They agreed that the sketch needed exact values and a clearer currency label, because the bars alone did not communicate the size of the differences.

**Participant 2 (student familiar with data visualization):** The participant also found the layout straightforward. They agreed that units and context mattered, especially clarifying that the values referred to enough food to provide **30 grams of protein**, rather than an ordinary serving size.

### What I learned and changed

Both participants responded positively to the simpler side-by-side layout, but the feedback made me realize that removing clutter is only helpful if the remaining labels are precise. I retained the two aligned charts and added cost and calorie values directly beside their bars. I clarified the currency (AUD), kept a common 30g protein basis, and added a source and reconstruction note. I also used different colors for the two measures so it was clear that they represented different quantities.

## Step 5: Final Tableau redesign

The final dashboard uses a blue horizontal bar chart for estimated cost and a purple horizontal bar chart for calories. Both charts use the same food order, sorted by cost, so a reader can move across a row without searching for a matching category. The value labels make exact reading easier than in the original, while the two charts preserve the differences between dollars and kilocalories.

**[Open the final interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/aditi.adgaonkar/viz/Book2_17943470761440/Dashboard1)**

<iframe src="https://public.tableau.com/views/Book2_17943470761440/Dashboard1?:showVizHome=no&:embed=true" width="100%" height="800" style="border:0;" title="Protein cost and calories dashboard" loading="lazy"></iframe>

### Data and interpretation notes

The source infographic publishes calorie values for each food and visual bar heights for prices, **not a downloadable table of exact prices**. For this redesign, I transcribed the ten calorie values and reconstructed approximate 2021 AUD costs from the original chart's vertical axis, rounded to the nearest AUD $0.10. Consequently, **the cost figures are estimates, not exact Woolworths transaction prices**, and should not be used as current grocery-price advice. This is a recreation of the original 30g comparison, not a new price survey.

The redesign is therefore best understood as an exercise in communicating an existing comparison more clearly, with its data limitations disclosed. The nutritional qualities of a food extend beyond cost and calories alone.

## Reflection

This project showed me that redesigning a chart is not the same as making it more decorative. The original already had a useful question and a sensible price ranking. Its weakness was that it made one variable much easier to compare than the other. The most useful change was not a new chart type, but separating cost and calories while keeping the food rows aligned.

The critique helped identify the issue, the sketch made the solution concrete, and feedback revealed the need for clearer units and values. In Tableau, I had to pay attention to sorting, consistent row order, labeling, and layout. I would improve this project further by obtaining original item-level pricing data to replace the approximate values, and by testing the finished dashboard with readers to see whether they can find meaningful comparisons quickly.

## Sources and references

- Radford-Smith, J. (2021, November 26). [*What Are The Cheapest High-Protein Foods?*](https://www.thebodybuildingdietitians.com/blog/how-cost-effective-is-your-high-protein-diet). The Bodybuilding Dietitians. Original chart and calorie values; cost source identified as Woolworths Australia.
- [MakeoverMonday](https://www.makeovermonday.co.uk/). February 20, 2023 challenge featuring the protein-cost visualization.
- Few, S. [*Data Visualization Effectiveness Profile*](https://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf).
- Berinato, S. (2016). *Good Charts: The HBR Guide to Making Smarter, More Persuasive Data Visualizations*. Harvard Business Review Press (Chapters 3–4).
- [Final redesign on Tableau Public](https://public.tableau.com/app/profile/aditi.adgaonkar/viz/Book2_17943470761440/Dashboard1).

## AI acknowledgment

I used ChatGPT to help interpret the assignment instructions, organize my critique using Stephen Few's framework, draft and revise explanatory text, and develop the redesign approach and Tableau steps. I also used an AI image generator to produce the hand-drawn-style wireframe image; it represents my intended design rather than measured data. ChatGPT assisted in preparing a reconstructed CSV from the source chart and suggested formatting and layout improvements for the Tableau dashboard. I reviewed the visualization, built the dashboard in Tableau Public, and shared the wireframe with two people for feedback. I have disclosed that the original exact price data was not available and that the reconstructed costs are approximate.

[Back to portfolio homepage](https://aadgaonkar.github.io/aditi-adgaonkar-portfolio/)
