# Travel Planner Based on Currency Conversion Risk
**Project Goal:**  Create a travel planning tool that will allow the user to select a set of countries they would like to travel to and a travel timeframe (3,6,12 months).  The tool will analyze historical Forex data and predict the country that will have the most favorable currency within the given travel timeframe.

**The tool will:**
Check Forex volatility as barometer for travel decisions
Use historical forex data (up to 2 years)
3 - 6 - 12 months predictive outlook using Monte Carlo and other algorithms
Produce graphs, risk graphs, value graphs,
Variables - currency / country,  traveling times (3-6-12 months)

**Questions:**
# #
- What is the variability of budget in base currency (USD) of the three locations selected ? 
- Rank the travel location by risk of currency fluctuation ( what is the risk? )
- Give the zone of values based on Monte-Carlo simulation is it wide closely similar etc based on locations selected/
- Is there correlation between weather variability and foreign currency variability

**Analysis**
# #
The tool is able to dynamically accept ( 3 ) countrues of origin determine the currency of the selected countries dynamically pull country information and statistics the using the Alpha Vantage API pull the Forex currency trading pair to determine the current value

We then normalize the values in the pair to USD denominator so that all the comparisons are based on USD value.

We then perform a MonteCarlo simulation to determine the range of values for that pair and compare the range and variance and display that information to the traveler in the form of graphs and summary text ( In the presentaton and code example select we chose periods of 3 months, 6 months and 12 months for time till traveling time frame.

The data source we had selected for dynamically pulling historical weather data fell thru as it was cost prohibitive for the amount of data  we needed. The free version of historical weather was limited to ( 3 ) days which is not useful for this analysis so it was scrapped from the resulting project

**Results:**

Example Country 1: Singapore
#

Example Country 2: Turkey
#

Example Country 3: United Kingdom
#

Comparison Statistics and Ratios

- Standard Deviations ( Daily ):
    - SGDUSD Daily Returns       0.003131
    - TRYUSD Daily Returns       0.012750
    - GBPUSD Daily Returns       0.005972
    - US Dollar Daily Returns    0.004215

- Standard Deviations ( Annuakized ):
    - SGDUSD Daily Returns       0.049708
    - TRYUSD Daily Returns       0.202403
    - GBPUSD Daily Returns       0.094802
    - US Dollar Daily Returns    0.066910
#
- Assets Riskier than the US Dollar
    - SGDUSD Daily Returns       False
    - TRYUSD Daily Returns        True
    - GBPUSD Daily Returns        True
    - US Dollar Daily Returns    False

