## CSV FILE  
### mock\_ops.csv data  
- timestamp  
- date  
- Zone  
- Shift  
- Pressure\_PSI  
- Temperature\_C  
- Flow\_Rate\_LPM

## API RESPONSE
### Open Meteo API \- past 1 month archived data
- timestamp  
- temperature\_2m  
- relative\_humidity\_2m  
- rain  
- weather\_code  
- precipitation  
- apparent\_temperature  
- surface\_pressure  

## DATABASE RETRIEVAL
### Merged and aligned data from both mock\_ops.csv and API response
#### All of the above fields, selected:
- timestamp  
- Zone  
- Pressure\_PSI  
- Flow\_Rate\_LPM  
- temperature\_2m  
- relative\_humidity\_2m  
- rain  
- weather\_code  
- precipitation  
- apparent\_temperature  
- surface\_pressure

My future improvements:  
-- arithmetically calculate throughput with appropriate formulas  
-- appropriate error handling  
-- better plots, translating the correlation well
