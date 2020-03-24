# COVID-19-Datata-Analysis

This project is part of The shortcut's python for data analysis training program .
In this project, I analyzed the spread of the new corona virus (nCov). 

- I was given the John Hopkins University's dataset which contains aggregated daily data for confirmed cases, deaths and recovered patients. 
https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series

Since the John Hopkins dataset contains only aggregated data, I needed to transform it into a format that allows me to answer more questions. I was given the ideal dataframe structure in picture .

I followed  the following instructions given by the instractor.
- Stack the dataframe so that each row represents one date in a location. 
- Remove the rows where the cumulative number of cases is zero.
- Make a new column `location` to combine `prov_state` and `country`.
- Make a new column `new_case` to derive the new case number from cumulative case number.
- Convert the date column to datetime object.

After transforming data for number of cases, I did the same for number of deaths and cureds.
Then instractor suggested to  use `pd.merge()` to merge them into one dataframe. Hint:  merging `case` with `death` first and then merge that with `cured`. A `left` merge on `['location', 'prov_state', 'country', 'lat', 'long', 'date']` columns
