**\#\# CSV FILE**  
**\#\#\# mock\_ops.csv data**  
\- timestamp  
\- date  
\- Zone  
\- Shift  
\- Pressure\_PSI  
\- Temperature\_C  
\- Flow\_Rate\_LPM

**\#\# API RESPONSE**  
**\#\#\# Open Meteo API \- past 1 month archived data**  
\- timestamp  
\- temperature\_2m  
\- relative\_humidity\_2m  
\- rain  
\- weather\_code  
\- precipitation  
\- apparent\_temperature  
\- surface\_pressure  

**\#\# DATABASE RETRIEVAL**  
**\#\#\# Merged and aligned data from both mock\_ops.csv and API response**  
**\#\#\#\# All of the above fields, selected:**  
\- timestamp  
\- Zone  
\- Pressure\_PSI  
\- Flow\_Rate\_LPM  
\- temperature\_2m  
\- relative\_humidity\_2m  
\- rain  
\- weather\_code  
\- precipitation  
\- apparent\_temperature  
\- surface\_pressure

My future improvements:  
\-- arithmetically calculate throughput with appropriate formulas  
\-- appropriate error handling  
\-- better plots, translating the correlation well

**2: The Data Integration (Show a diagram of how you combined API \+ DB \+ Internal Data).**

![][image1]

**3: The Insight & Recommendation (What did the merged data reveal?).**

Temperature vs Flow Rate Correlation: 0.01

                             Zone  Pressure\_PSI  Flow\_Rate\_LPM  \\  
timestamp                                                          
2026-06-25 02:00:00     Zone\_East    160.157953     673.194158     
2026-06-26 21:00:00    Zone\_South    184.513951     716.486706     
2026-06-30 08:00:00     Zone\_East    205.383753     716.968183     
2026-06-27 02:00:00  Zone\_Central    201.468924     723.548105     
2026-07-01 11:00:00  Zone\_Central    201.464269     743.424002   

                     temperature\_2m  relative\_humidity\_2m  rain  weather\_code  \\  
timestamp                                                                         
2026-06-25 02:00:00       19.000000             87.074471   0.0           1.0     
2026-06-26 21:00:00       25.600000             67.763252   0.0           0.0     
2026-06-30 08:00:00       20.750000             78.373680   0.0           3.0     
2026-06-27 02:00:00       14.600000             78.747032   0.0           0.0     
2026-07-01 11:00:00       18.299999             67.588943   0.1          51.0   

                     precipitation  apparent\_temperature  surface\_pressure    
timestamp                                                                     
2026-06-25 02:00:00            0.0             19.571442        931.741638    
2026-06-26 21:00:00            0.0             25.459936       1014.429260    
2026-06-30 08:00:00            0.0             21.596422        933.054871    
2026-06-27 02:00:00            0.0             13.795815        838.362915    
2026-07-01 11:00:00            0.1             18.233372        841.232178    
Zone                        str
