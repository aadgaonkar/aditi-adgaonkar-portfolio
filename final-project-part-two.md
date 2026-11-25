# The NYC Café Dilemma · Final Project Part II

Aditi Adgaonkar · Telling Stories with Data · Carnegie Mellon University

[Portfolio home](https://aadgaonkar.github.io/aditi-adgaonkar-portfolio/) · [Part I](https://aadgaonkar.github.io/aditi-adgaonkar-portfolio/nyc-cafe.html) · [Shorthand storyboard](https://preview.shorthand.com/Odbxgnwgfm1XnQHW) · [Part III](final-project-part-three)

## Storyboard and draft visualizations

During fall break, I noticed coffee shop after coffee shop on a walk through the West Village. What made each new owner think there was room for one more? I followed that question to five Manhattan corridors where public pedestrian counts and asking rents could be matched. The story is for first-time independent café owners evaluating a storefront.

| Story beat | What the reader sees | What it helps the reader do |
|---|---|---|
| What’s already nearby? | Maps showing Coffee/Tea establishments within 400 meters of each pedestrian count point | See where nearby coffee options cluster. |
| Who passes in the morning? | A bar chart comparing sampled weekday pedestrian counts from 7 to 9 a.m. | Compare how many people pass each location during the morning window. |
| Do busier streets have higher asking rents? | A scatterplot comparing morning pedestrian counts with average asking rent and labeling each point with its nearby café count | Compare the tradeoffs across the five corridors. |
| What would make someone choose your café? | An example of a weekday takeaway café near Herald Square | Use the charts to decide what to observe, what to ask customers, and what to verify about the rent for a specific space. |

Part I feedback asked for a stronger connection between the visuals and the ending. The Herald Square example now reuses the same pedestrian count, nearby café count, and rent benchmark from the charts. It also gives readers a reason to investigate customer loyalty and recognition directly.

## Sources and methods

- [NYC DOT Bi-Annual Pedestrian Counts](https://data.cityofnewyork.us/Transportation/Bi-Annual-Pedestrian-Counts/cqsj-cfgu) and [counting methodology](https://www.nyc.gov/html/dot/downloads/pdf/bi-annual-ped-count-readme.pdf). The chart compares sampled May 2026 weekday morning counts at one point per corridor.
- [NYC restaurant inspection records](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j/about_data). I counted distinct Coffee/Tea establishment IDs within 400 meters of each count point, measured in a straight line. The November 24, 2026 snapshot may omit coffee sellers in other categories and include permit applicants.
- [REBNY Manhattan Retail Report, First Half 2026](https://www.rebny.com/reports/manhattan-retail-report-first-half-2026/). The chart uses average ground-floor retail asking rents in dollars per square foot per year. These are corridor benchmarks. A specific storefront may have different lease terms.

## User research protocol

**Goal.** Find out whether readers can interpret the visuals and use them to decide what to investigate before choosing a café location.

**Audience and recruitment.** The intended audience is first-time independent café owners who are comparing storefronts. For this initial review, I shared the draft with three readers from different professional backgrounds. Their feedback gives me an initial read on whether the story is understandable. To test whether the story is useful for the intended decision, I would recruit people actively considering their first café and owners who recently chose their first location. I would look for people who have compared at least two storefronts and ask them to apply the story to an address they are considering or have considered.

**Interview script.** Ask readers to scroll through the draft and explain what they see before offering any clarifications. Ask permission before taking anonymous notes or using a direct quote.

1. After the opening, what question do you think the story is trying to answer?
2. What do the dots and the circle on the café map represent?
3. Why do you think the story focuses on 7–9 a.m.? What can you tell from the pedestrian count?
4. How would you explain the difference between Herald Square and Upper Fifth Avenue to a friend?
5. If you were considering a storefront near Herald Square, what would you do next? Which part of the story helped you decide?
6. Was there anything you had to reread or guess?

After questions 2, 4, and 5, ask readers to point to what informed their answer. Record what each reader understood independently, where they needed a prompt, and whether they could name a concrete next step for a storefront.

## User research findings

I shared the Shorthand draft with three reviewers. The draft asks readers to consider foot traffic, asking rent, and nearby cafés when evaluating a storefront.

| Reviewer | Background | Recorded response |
|---|---|---|
| P1 | Software developer | Reviewed the draft and agreed with the overall argument. |
| P2 | Guitarist | Reviewed the draft and agreed with the overall argument. |
| P3 | Doctor | Reviewed the draft and agreed with the overall argument. |

The reviewers agreed with the overall premise. Three more specific points came up across the reviews:

- **Asking rent.** The $412 figure was read as the rent for a particular storefront. It represents Herald Square’s average annual asking rent per square foot for ground-floor retail.
- **Morning foot traffic.** The reason for comparing pedestrian counts from 7 to 9 a.m. was unclear. The time window matters for the weekday takeaway café scenario.
- **Customer behavior.** A question the charts raised was where people actually stop to buy coffee and what makes them return. That is something a prospective owner could investigate on a site visit.

I summarized these observations across the reviews. The individual entries above record the response I can attribute to each reviewer.

## Planned revisions for Part III

| Evidence or observation | Planned Part III change | How I would test it |
|---|---|---|
| The $412 benchmark could be read as the asking rent for one storefront. | Label the figure directly as **corridor average annual asking rent per square foot**. In the Herald Square example, ask the reader to get a quote for the specific space. | Ask readers to explain what $412 measures and what number they still need from the landlord or broker. |
| The reason for showing 7–9 a.m. foot traffic was unclear. | Introduce the weekday takeaway café before showing the pedestrian chart so the reader knows why the morning window matters. | Ask readers why the chart uses that time window and whether it would suit a café with different opening hours. |
| The review raised a question about where people stop for coffee and why they return. Part I instructor feedback also raised loyalty, brand recognition, and how long cafés have operated. | Add a site-visit checklist to the ending. Pick an address, visit during planned opening hours, observe where people stop, ask what brings them back, and check how long the cafés they mention have been open. | Ask each reader to name the first thing they would check in person and explain which part of the story prompted it. |

## Conclusion

Herald Square had more observed morning pedestrians than Upper Fifth Avenue in this sample, even though its corridor had lower average asking rent. The café maps show the nearby options a new owner would need to understand. For Part III, I want to make it easier for readers to turn those observations into a plan for evaluating one storefront.

## AI acknowledgment
I developed the research question from my own observations in the West Village, decided what the story should help first-time café owners do, and conducted the user interviews myself. I interpreted the findings and made the final decisions about the story and its conclusions. I used CoPilot to help match the public datasets, calculate café counts within 400 meters of each pedestrian count point, build the draft charts, and edit the write-up. I reviewed everything generated by AI again before finalising.
