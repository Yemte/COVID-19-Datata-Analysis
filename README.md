# COVID-19-Datata-Analysis

This project is part of The short cuts's python for datanalysis training program .
In this project, we will analyze the spread of the new corona virus (nCov). We will use two datasets:

- The John Hopkins University's dataset which contains aggregated daily data for confirmed cases, deaths and recovered patients. 
https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series

Since the John Hopkins dataset contains only aggregated data, we need to transform it into a format that allows us to answer more questions. You can see the ideal dataframe structure in the picture below.

I followed  the following instructions given by by the instractor.
- Stack the dataframe so that each row represents one date in a location. 
- Remove the rows where the cumulative number of cases is zero.
- Make a new column `location` to combine `prov_state` and `country`.
- Make a new column `new_case` to derive the new case number from cumulative case number.
- Convert the date column to datetime object.

After transforming data for number of cases, I did the same for number of deaths and cureds.
Then instractor suggested to  use `pd.merge()` to merge them into one dataframe. Hint:  merging `case` with `death` first and then merge that with `cured`. A `left` merge on `['location', 'prov_state', 'country', 'lat', 'long', 'date']` columns
