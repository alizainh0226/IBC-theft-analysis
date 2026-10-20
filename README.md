# The Theft Tax: What's Driving Ontario Auto Insurance Costs?

Newer cars cost more to insure mainly because they're expensive to repair. Theft makes it worse, but mostly for cars that were already expensive.

## Guiding question
What makes newer cars more expensive to insure, and how much of it is theft?

## Key findings
- **Repair costs are the main driver.** Collision and property damage ratings climb from about 15 for 1998 models to 125–160 for recent ones, while the typical recent car is below average on theft. Premiums rose fastest in rural areas, not the theft-heavy GTA, which is consistent with repair costs affecting everyone.
- **Theft stacks on cars that are already expensive.** Only 27% of recent vehicles are high-theft, but two-thirds of those are also expensive to repair.
- **The metric changes the answer.** Ranked by count, Toyota had the most high-theft models. Ranked by rate, Land Rover (95%) and luxury brands led.
- **The pure theft tax is rare.** Only 13 vehicles, mostly trucks and 4x4s like the Wrangler and Silverado, are cheap to insure on everything except theft.

## Charts
![Claim costs by model year](Charts/chart_3.png)
![Theft risk by make](Charts/chart_4.png)
![Repair cost vs theft](Charts/chart_5.png)
![Ontario premium growth](Charts/chart_6.png)

## Data
- **IBC How Cars Measure Up 2026:** claim cost ratings for about 5,800 vehicles (1998–2026 model years). Download it from IBC's website; the raw file isn't included in this repo.
- **FSRA:** average Ontario auto insurance premiums by region (Oct 2024 – Jun 2026).
- **Équité Association:** most-stolen vehicle lists, used to cross-check theft findings.

## Methods
- Cleaned the IBC workbook: fixed header rows, removed empty spacer columns, stripped hidden spaces from column names.
- Investigated a theft value of 1.0 appearing in 37% of rows and confirmed it as a "no theft claims" floor value.
- Used medians instead of means because of extreme outliers.
- Excluded 2026 models because their claim data is immature.
- Compared brands by rate as well as count, and used a log scale to show theft values ranging from 1 to 8,248.

## Limitations
- Ratings are claim cost indexes, not actual premiums. The link to premiums is consistent with the findings but doesn't prove cause.
- Comparing model years today mixes design with age. Older cars are worth less, are driven less, and may not carry collision coverage.
- Model variants are not weighted by popularity, and some vehicles appear twice under different brands, like the Chevrolet Silverado and GMC Sierra.
- The data shows which cars are stolen, but not why.

## What I'd do next
- Compare past HCMU editions to track how specific models' ratings change over time.
- Add vehicle prices to separate a car's value from how it was designed.

## Tools
Python (pandas, matplotlib), Google Colab
