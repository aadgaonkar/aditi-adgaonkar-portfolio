# The NYC Café Dilemma: Is the Busiest Street the Best Street?

**Telling Stories with Data | Final Project, Part I**  
**Format:** Proposal, initial sketches, identified public datasets, and proposed medium  
**Status:** Design proposal; no empirical corridor rankings have been made

[Back to portfolio](../index.html) | [See data sources](data/source_catalog.csv) | [Sketch 1](sketches/01_foot_traffic.png) | [Sketch 2](sketches/02_tradeoffs.png) | [Sketch 3](sketches/03_decision.png)

## 1. Project outline

### High-level summary

A first-time café owner in New York City might instinctively look for the busiest street. More people walking by means more potential customers, right? But foot traffic is only the beginning of the decision. Popular commercial corridors can also come with high retail asking rents and existing cafés competing for similar customers. A street with slightly fewer passersby might be worth a closer look if the occupancy cost is more manageable. This project asks how an aspiring independent café owner can narrow down location options using evidence rather than street reputation alone.

I want to build a short, interactive story comparing a few **Manhattan commercial corridors that have overlapping public data**, rather than producing a broad ranking of every NYC neighborhood. The analysis will use NYC DOT pedestrian observations to represent potential exposure, NYC restaurant inspection records to approximate nearby coffee and tea competition, and REBNY retail reports to understand published asking rents. These measures cannot predict a café's sales or success, so the goal is to develop a practical **shortlist for follow-up site visits and lease research**, not to declare a guaranteed winner.

### Audience, purpose, and intended message

My primary reader is someone considering their first independent café in NYC. They may understand coffee and customers but not know how to compare locations systematically. By the end, I want them to question the assumption that the busiest street is automatically best and recognize the tradeoffs of exposure, competition, and cost. The decision this project helps with is simple: **Which corridors are worth investigating next, and what risks should the owner check in person?**

**One-sentence message:** A promising café location is not necessarily the busiest one; it is one where pedestrian exposure, competitors, and occupancy cost make sense together.

### The story arc

**Act 1: The easy answer.** Open on a bustling NYC street with the question, “Is this where you would open a café?” Present a straightforward comparison of pedestrian counts at matched DOT locations. **Reader takeaway:** Foot traffic is useful, but it captures only part of the business opportunity. **Visual:** An annotated horizontal bar chart, with explicit observation windows and sample-point labels (Sketch 1).

**Act 2: The complication.** Add published asking rents and approximate nearby café density. Show corridors on a scatterplot, where horizontal position indicates pedestrian activity, vertical position indicates asking rent, and circle size indicates nearby café count. The point is not to create a score but to reveal possible tradeoffs. **Reader takeaway:** A high-traffic location can carry significant cost and competitive pressure. **Visual:** Annotated scatterplot with size legend and source notes (Sketch 2).

**Act 3: The practical decision.** End with a comparison of two or three qualifying locations. Explain why each might deserve a site visit and what remains unknown, such as exact storefront lease terms, morning customer mix, conversion to purchases, and weekend patterns. **Reader takeaway:** Use the data to choose what to investigate, not to predict profits. **Visual:** Shortlist comparison table with caveats and a clear next step (Sketch 3).

### Scope and evidence rule

The geographical scope is **Manhattan retail corridors represented in the REBNY report** that can also be paired with NYC DOT counting locations. SoHo/Broadway, the Union Square vicinity, and other major corridors are starting points for checking overlap, **not confirmed or ranked study sites**. I will select approximately three to five corridors after inspecting the source tables. If count locations and rent corridor boundaries do not match, I will reduce the comparison rather than make up a proxy. The actual cafés will be filtered by type and geography, with the definition and walking radius documented before analysis.

### Research questions

1. Which eligible sampled corridors have higher pedestrian exposure in comparable count periods?
2. How many observable coffee/tea establishments are in a consistently defined nearby area?
3. How do REBNY retail asking rents compare across the eligible corridors?
4. Are there plausible tradeoffs between visibility, competitive density, and rent that change which corridors deserve follow-up?
5. Which missing details would have to be checked before signing a lease?

## 2. Initial sketches

The sketches below show the **planned reader experience**. They are deliberately not final Tableau charts, and the points, bubble sizes, and bars are hypothetical visual placeholders, **not measurements**. Their job in Part I is to demonstrate what readers would see and how the story would unfold.

### Sketch 1: Start with the crowd

![Annotated sketch showing story context and a properly labeled horizontal bar chart for pedestrian counts](sketches/01_foot_traffic.png)

The first screen challenges the intuitive appeal of the busiest street. It pairs an easy-to-follow narrative with a bar chart of pedestrian observations. The final version will show the actual DOT locations, count window, sampling date, and observed pedestrians. The same time basis will be used throughout, and locations without compatible observations will be excluded.

### Sketch 2: Introduce rent and competitors

![Annotated scatterplot sketch with foot traffic on x-axis, retail rent on y-axis, and café count as point size](sketches/02_tradeoffs.png)

Each circle will represent one eligible corridor, not one individual café. Hover text will show its count location, observation period, rent basis and source, and how the nearby competition total was defined. The story will highlight tradeoffs, not assume that larger bubbles automatically mean a worse location.

### Sketch 3: Turn evidence into a shortlist

![Sketch of a corridor decision table with foot traffic, rent, café density, and questions to verify](sketches/03_decision.png)

The final visual will bring the measures together into two or three candidate summaries. It will show both reasons to explore a site and reasons to hesitate. The closing message will encourage field checks and avoid a misleading single-number “best café” ranking.

## 3. Data sources, access, and intended use

I plan to use three publicly accessible primary sources. **First**, NYC DOT's [Bi-Annual Pedestrian Counts](https://data.cityofnewyork.us/Transportation/Bi-Annual-Pedestrian-Counts/cqsj-cfgu) gives pedestrian observations at selected locations. I will use these counts as an indicator of visibility, not of customers or sales. The DOT explains that observations come from sampled sites; the [methodology document](https://www.nyc.gov/html/dot/downloads/pdf/bi-annual-ped-count-readme.pdf) notes that a zero can mean that no data was collected. I will keep count dates, intervals and locations comparable, and avoid interpreting missing observations as no pedestrians.

**Second**, the [NYC Department of Health and Mental Hygiene Restaurant Inspection Results](https://data.cityofnewyork.us/Health/NYC-Restaurant-Inspection-Results/gv23-aida) dataset provides establishment records that can help identify nearby coffee and tea businesses. These rows describe inspections, so they should not be counted as if every row were a different café. I plan to deduplicate by the unique restaurant identifier **CAMIS**, check category labels and coordinates, and define a consistent nearby area around each sample street. This will be a transparent approximation of existing competition, not a complete list of every café or a direct measure of demand.

**Third**, the [REBNY Manhattan Retail Report, First Half 2026](https://www.rebny.com/reports/manhattan-retail-report-first-half-2026/) provides a published overview of retail asking rents across selected Manhattan corridors. I plan to extract the relevant published rent figures and retain the stated units, corridor definitions, and reporting period. Asking rent is not a signed café lease, and it can vary across storefronts within the same street. Combining this evidence with pedestrian counts should make it possible to tell a more nuanced story than foot traffic alone. The dates and geographies will not match perfectly, and those differences will be disclosed on the final page.

### Direct public data access

| Source | Public link | What I will extract |
|---|---|---|
| NYC DOT pedestrian count data | [Open dataset](https://data.cityofnewyork.us/Transportation/Bi-Annual-Pedestrian-Counts/cqsj-cfgu) | Sample location, count window, pedestrian count |
| NYC DOHMH inspection data | [Open dataset](https://data.cityofnewyork.us/Health/NYC-Restaurant-Inspection-Results/gv23-aida) | CAMIS, business category, coordinates/address |
| REBNY retail asking rents | [Open H1 2026 report](https://www.rebny.com/reports/manhattan-retail-report-first-half-2026/) | Corridor, published asking rent, reporting units |
| NYC DOT data documentation | [Read methodology](https://www.nyc.gov/html/dot/downloads/pdf/bi-annual-ped-count-readme.pdf) | Sampling and missing-value definitions |

A machine-readable [source catalog](data/source_catalog.csv) is also included in this project, listing links and planned uses. These are **live public data sources**, not privately held data. This is a planning deliverable: data source access is identified, but **corridor-level results have not been calculated**. The project will not present hypothetical sketch values as empirical evidence.

### Preparation and safeguards

I will use only corridors with demonstrably compatible count points and retail rent coverage. I will note the timestamp and units for each pedestrian observation, use a consistent geographic boundary for café counts, deduplicate restaurant records by CAMIS, and preserve the REBNY report's exact rent definition. If a comparison lacks comparable observations, I will disclose the gap or remove that corridor. The final project will distinguish data, assumptions, and interpretation, and cite all visuals using official source URLs. This is an original proposed cross-dataset comparison, not a copy of an existing Tableau dashboard.

## 4. Method and medium

For the completed final project, I will create an interactive, standalone narrative using **Tableau Public** for the annotated bar chart, scatterplot, and corridor comparison, and **GitHub Pages (HTML/CSS)** to arrange the visualizations in a scrollable story. The reader will move through the three acts rather than see an isolated dashboard. Tableau hover tooltips will explain units and data provenance. I will design my own graphics and use linked public sources. No PowerPoint or Excel file will be the final medium.

## 5. Limits and closing question

This work measures signals, not profitability. Observed pedestrians do not equal customers, nearby cafés do not prove unmet demand, and asking rents are not exact lease costs. The concluding question will be: **Which two streets should a small café owner actually visit, and what would they need to learn there before committing?**

## References

- New York City Department of Transportation. *Bi-Annual Pedestrian Counts*. NYC Open Data.
- New York City Department of Transportation. *Bi-Annual Citywide Pedestrian Counts: Readme and Methodology*.
- New York City Department of Health and Mental Hygiene. *NYC Restaurant Inspection Results*. NYC Open Data.
- Real Estate Board of New York. *Manhattan Retail Report, First Half 2026*.
