# Carbon-sense-webapp
CarbonSense: a carbon footprint calculator that estimates a user’s emissions from travel, electricity and food, and suggests how to reduce them, built around core DAA algorithms.

 CarbonSense

CarbonSense is a carbon footprint tracking app. A user enters daily activities
(travel, electricity use and food type), and the app calculates their carbon
score, classifies the level as Low, Medium or High, and suggests how to reduce
emissions. The project applies core Design and Analysis of Algorithms (DAA)
concepts to a real-world problem.

## Problem Statement
Carbon emissions are rising, and most people have no simple way to see how
their daily habits contribute. CarbonSense makes this visible and promotes
eco-friendly habits.

## Objectives
- Calculate a user's carbon footprint from daily activities
- Classify the result and show it clearly
- Promote eco-friendly habits through targeted suggestions
- Offer free and premium access levels

## App Flow
1. **Login / Start:** user enters a name and starts
2. **Activity Input:** travel (km), electricity (units) and food type
3. **Calculate:** pressing the button runs the algorithm
4. **Result:** carbon score and level (Low / Medium / High)
5. **Report / Tips:** free users get general tips, premium users get a detailed report

Example: Travel = 10 km, Electricity = 5 units, Food = non-veg
`carbon = (10 x 0.21) + (5 x 0.85) + foodFactor`

## Algorithms Used

| # | Feature | Algorithm Type | Time | Space |
|---|---------|----------------|------|-------|
| 1 | Carbon calculation | Iterative | O(n) | O(1) |
| 2 | Carbon level (Low/Medium/High) | If-Else decision | O(1) | O(1) |
| 3 | Weekly / monthly report | Aggregation (sum) | O(n) | O(1) |
| 4 | Comparison report (emission ranking) | Merge Sort (divide and conquer) | O(n log n) | O(n) |
| 5 | Suggestion engine | Greedy (target highest emission category) | O(n) | O(1) |

### Carbon Level Rules
- Below 5: Low
- 5 to below 10: Medium
- 10 and above: High

## Free vs Paid Logic
A trial counter tracks premium usage. If the trial count is below 3, premium
features are allowed; otherwise they are blocked.

## Data Structures
Arrays, lists and structures (records) for activities, factors and daily totals.

## System Architecture
User Input -> Algorithm -> Result -> Suggestions

## Tech Stack
Python, Django, HTML5, CSS3, Bootstrap, SQLite

## How to Run
1. Clone the repository
2. Install libraries: pip install -r requirements.txt
3. Run migrations: python manage.py migrate
4. Start the server: python manage.py runserver

## Conclusion
CarbonSense calculates and analyzes personal carbon footprints using efficient
algorithms and structured data handling. It combines real-world features such
as free and premium access with environmental awareness, and shows practical
applications of DAA concepts.
