#EU Carbon Policies Regression Analysis

**(1) OVERVIEW**<br>
I use panel data from 1970 to 2023 to uncover whether EU membership, and therefore the eurozone-exclusive cap-and-trade system, reduces carbon emissions in European countries. 

**(2) DATA**<br>
Source: World Bank Open Data(https://data.worldbank.org/).<br>
Processing: Cleaned and formatted for regression analysis. 

**(3) METHODOLOGY**<br>
I used a regression model with country- and time- fixed effects as well as three interaction terms between EU membership status and political stability, rule of law, and voice and accountability (the World Governance Indicators, or WGIs). It explains 35% of the variation in carbon emissions. The emprical model is as follows:

CO2Em_it = β0 + β1 EU_it + β2 PolSt_it + β3 RoL_it + β4 VaA_it 
           + β5 (EU_it * PolSt_it) + β6 (EU_it * RoL_it) + β7 (EU_it * VaA_it) 
           + δ0 dt_t + α_i + u_it

Where EU is EU membership status (1 if in EU, 0 if not in EU), CO2Em is the metric tons of CO2 emissions, PolSt is political stability, PoL is rule of law, and VaA is voice and accountability. 
β1 was hypothesized to be negative since EU members benefit from an eurozone-exclusive cap-and-trade system. 

**(4) FINDINGS**<br>
The regression analysis showed that the three interaction terms between EU membership and PolSt, RoL, and VaA are statistically significant, while the main coefficient (β1) is not. This indicates that the effect of EU membership on carbon emissions may be moderated by the type/quality of governance in the country, but membership itself is not found to be correlated with lower emissions. 
