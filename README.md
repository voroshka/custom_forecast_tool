The following script builds a FBProphet forecast for uplift modelling used for Geo based AB testing. In particular it is used for incrementality testing of marketing channels; marketing campaigns with the use of TV or other offline channels. 

The script takes as inputs:
- Forecast parameters filled in by the managers in the GoogleSheet file. Parameters are imported using Google API. 
- Historical data of at least 3 years for each forecast. The data is imported from connected database (Vertica in this case) using SQL builder. 
The script provides as outputs:
- Factual data for the given dates
- Foreacsted (simulated) data for the given dates
- Error of the model (accuracy)
- Visualisation


The script consists of the following: 
1. Libraries import 
2. Functions activation
3. Forecast input parameters downloading
4. Main code (one iteration for each forecast)
    1. Data uploading
    2. Data preprocessing
    3. Exogenous variable selection
    4. FBProphet parameters tuning 
    5. Model fitting 
    6. Visualisation 
5. Export of the results to DataBase 
