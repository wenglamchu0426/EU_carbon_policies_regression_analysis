#EU Carbon Policies Regression Analysis

**(1) OVERVIEW**<br>
I use panel data from 1970 to 2023 to uncover whether EU membership, and therefore the eurozone-exclusive policies, reduces carbon emissions in European countries. 

**(2) DATA**<br>
Source: World Bank Open Data(https://data.worldbank.org/).<br>
Processing: Cleaned and formatted for regression analysis. 

**(3) METHODOLOGY**<br>
I used a regression model with country- and time- fixed effects as well as three interaction terms between EU membership status and political stability, rule of law, and voice and accountability (the World Governance Indicators, or WGIs). It explains 35% of the variation in carbon emissions. The empirical model is as follows:

CO2Em_it = β0 + β1 EU_it + β2 PolSt_it + β3 RoL_it + β4 VaA_it 
           + β5 (EU_it * PolSt_it) + β6 (EU_it * RoL_it) + β7 (EU_it * VaA_it) 
           + δ0 dt_t + α_i + u_it

where:<br>
EU = EU membership status (1 if in EU, 0 if not in EU)<br>
CO2Em = metric tons of CO2 emissions<br>
PolSt = political stability<br>
PoL = rule of law<br>
VaA = voice and accountability<br>

and:<br>
β1 was hypothesized to be negative. 

**(4) FINDINGS**<br>
The regression results indicate that all three interaction terms between EU membership and the WGIs are statistically significant, while the main coefficient β1 is not. This suggests that EU membership by itself is not directly associated with lower emissions. Rather, the effect of EU membership on emissions depends on the quality of governance: countries with higher political stability, stronger rule of law, and greater voice and accountability experience more substantial reductions in CO2 emissions.
