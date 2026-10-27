| [home page](https://aadgaonkar.github.io/aditi-adgaonkar-portfolio/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique 1: When did states give married women property rights?

**Graphic:** NCSL "Map Monday" map of the year states adopted laws giving women the right to own property.
Source: National Conference of State Legislatures (NCSL), "Map Monday: Written in 1839, Still the Law Today: Married Women's Property Act" (page headed "Married Women Granted Right to Control Their Property"), updated July 20, 2026.

![Original NCSL map of the year states adopted laws giving women the right to own property](images/ncsl-original-map.png)

## What I see first
My eyes went to the large western states on the dark map before I read the title. I could tell the map compares states, but I couldn't tell which states acted first. I had to keep looking from the map to the legend to decode the colors.

Looking closer, the legend runs from 1848-1859 to 1940-1959, but it skips from 1900-1919 to 1940-1959. Does that mean no states fall in 1920-1939, or is an interval missing? The map doesn't say. The teal, red, blue and green also look like separate categories rather than a timeline. Small Northeast states are hard to identify, and the "Switch View" button makes this feel like a screenshot instead of a finished static chart.

My main question was: what should I learn from this map? Is it showing where change started, how it spread, or when my state passed a law?

## What I like, dislike and wish I saw

| Design dimension | Like | Dislike / wish |
|---|---|---|
| Typography | The title tells me this is a map of when states passed laws. | The title is small, and "women" sounds broader than laws about *married* women. I'd enlarge it, name married women, and explain that the laws varied by state. |
| Color | Filled states show that different regions fall into different periods. | Seven unrelated colors make the years hard to read in order. I'd use seven shades of one blue-green, light for early and dark for late. |
| Visualization type | A U.S. map suits state laws, and the familiar outline helps me find regions. | Large states stand out more than small ones even though each state is one observation. I'd keep the map but add a state lookup and a Northeast callout. |
| Cognition | The legend lets me find a state's period if I take the time. | Reading each state takes repeated trips between the map and key. A short note on the legal subject and a direct lookup would help. |
| Scale | State boundaries fit the data, and the legend shows periods rather than exact years. | The periods are uneven and jump from 1900-1919 to 1940-1959 without explanation. I'd keep the verified groupings but explain the missing interval. |

## Three changes I would make

1. **Use an ordered color scale instead of seven unrelated colors.** Assign the seven existing periods seven ordered blue-green shades, light for earlier adoption and dark for later, and keep the date-range labels. This makes the time pattern easier to scan.
2. **Make the title more specific.** Use "When states adopted married women's property laws" with the subtitle "Timing differed across states, and the laws did not grant identical rights." This is more precise about who gained rights and what the laws meant.
3. **Help readers find specific states.** Use selective two-letter state labels, with a small Northeast inset for states too narrow to label. That makes individual states easier to identify without cramming names into the map.

## Final design recommendations

**1. Make adoption periods readable.** Keep the same states and seven source date categories, but replace the rainbow with an ordered blue-green scale, earliest to latest: `#E6F3F1`, `#C5E3DC`, `#98CFC3`, `#65B5A8`, `#338F8A`, `#1C676F`, `#123E54`. Put the legend right next to the map, list each interval in chronological order, and label the scale "Earlier adoption" to "Later adoption." Use 11 pt dark text and narrow white state borders, and test the palette in grayscale and a color-vision simulator. Do not invent a 1920-1939 category; check the source first. If there are truly no observations, add the note "No states shown for 1920-1939" next to the legend.

**2. Explain the subject and lead with the point.** Replace the heading with "When states adopted married women's property laws" in 21 pt bold, add the 12 pt subtitle "Timing differed across states, and the laws did not grant identical rights," and add the note "Colors show adoption periods, not exact enactment years or equal legal protections." Keep the source in 9 pt below the map. For a static version, crop out "Switch View" and replace the black canvas with off-white (`#FAFBFC`) and dark gray (`#263238`) text.

**3. Make small states findable.** Use two-letter abbreviations only where they fit at 8 pt or larger. For the crowded Northeast, add a small enlarged inset with thin leader lines and readable labels, with each state's color matching the main map. Add an optional alphabetical lookup titled "State | Adoption period," filled only with the ranges the source actually supplies.

## Good Charts Matrix score

![Good Charts Matrix showing the original graphic scored at -3 design execution and -2 contextual awareness](images/good-charts-matrix.png)

**Design execution: -3.** A recognizable U.S. map is a reasonable form for state laws, but the mixed colors, small title and separate legend make comparison harder.
**Contextual awareness: -2.** The topic is important, yet the map doesn't explain how the laws differed or why the timeline omits 1920-1939.
Both scores describe the original image, not my redesign.

## Reflection
I relied mostly on what I noticed myself: the map and legend felt disconnected, and the smaller states were hard to identify. Reviewing my ideas for new problems showed that similar neighboring shades and crowded labels could undo them, so I chose selective labels with an inset. I also kept the map's source-defined periods instead of inventing exact years. I still want the underlying data checked to explain the 1920-1939 jump. A cleaner design can't fix gaps in the source documentation.

## References
- Berinato, S. (2016). *Good charts: The HBR guide to making smarter, more persuasive data visualizations.* Harvard Business Review Press.
- Berinato, S. (2019). *Good Charts Workbook: Tips, tools, and exercises for making better data visualizations* (Chapter 1: Controlling Color). Harvard Business Review Press.
- National Conference of State Legislatures. (2026, July 20). Map Monday: Written in 1839, still the law today: Married Women's Property Act. https://www.ncsl.org/resources/map-monday-married-women-granted-right-to-control-their-property

## AI acknowledgements
I used a generative AI assistant to critique my three recommendations and to suggest three of its own. I made the final decisions. Claude also helped me write up this page from my submitted critique.
