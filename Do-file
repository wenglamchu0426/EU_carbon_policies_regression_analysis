sum EU CEmissionspc GDPpc GovDebt PoliticalStability RuleofLaw VoiceandAccountability
outreg2 using "SummaryStatistics.doc", replace sum(log) keep (EU CEmissionspc GDPpc GovDebt PoliticalStability RuleofLaw VoiceandAccountability)

reg CEmissionspc EU if Time == 2019, r 
outreg2 using "ResultsTable.doc", replace label ctitle(OLS) title("Regression Models") adjr2

xtreg CEmissionspc EU GDPpc GovDebt PoliticalStability RuleofLaw VoiceandAccountability, r fe
outreg2 using "ResultsTable.doc", append label ctitle(Ind.FE) addtext(Individual FE, YES) adjr2

xtreg CEmissionspc EU GDPpc GovDebt PoliticalStability RuleofLaw VoiceandAccountability i.Time, r fe
outreg2 using "ResultsTable.doc", append label ctitle(Ind.FE/Time FE) keep(CEmissionspc EU GDPpc GovDebt PoliticalStability RuleofLaw VoiceandAccountability) addtext(Individual FE, YES, Time FE, YES) adjr2

test GDPpc GovDebt

xtreg CEmissionspc EU EU#c.PoliticalStability PoliticalStability RuleofLaw VoiceandAccountability i.Time, r fe

outreg2 using "ResultsTable.doc", append label ctitle(Ind.FE/Time FE) keep(CEmissionspc EU EU#c.PoliticalStability PoliticalStability RuleofLaw VoiceandAccountability) addtext(Individual FE, YES, Time FE, YES) adjr2

xtreg CEmissionspc EU EU#c.PoliticalStability EU#c.RuleofLaw PoliticalStability RuleofLaw VoiceandAccountability i.Time, r fe

outreg2 using "ResultsTable.doc", append label ctitle(Ind.FE/Time FE) keep(CEmissionspc EU EU#c.PoliticalStability EU#c.RuleofLaw PoliticalStability RuleofLaw VoiceandAccountability) addtext(Individual FE, YES, Time FE, YES) adjr2

xtreg CEmissionspc EU EU#c.PoliticalStability EU#c.RuleofLaw EU#c.VoiceandAccountability PoliticalStability RuleofLaw VoiceandAccountability i.Time, r fe

outreg2 using "ResultsTable.doc", append label ctitle(Ind.FE/Time FE) keep(CEmissionspc EU EU#c.PoliticalStability EU#c.RuleofLaw EU#c.VoiceandAccountability PoliticalStability RuleofLaw VoiceandAccountability) addtext(Individual FE, YES, Time FE, YES) adjr2

collapse (mean) CEmissionspc, by(Time EU)
twoway (line CEmissionspc Time if EU == 1, lcolor(blue)) (line CEmissionspc Time if EU == 0, lcolor(red)), legend(label(1 "EU") label(2 "Non-EU")) ytitle(`"Mean Mt CO2 Emissions Per Capita"') title("EU vs Non-EU Trends in CO2 Emissions")
