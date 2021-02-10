## California’s layoffs and closures of 2019 and 2020 by Big Local News

The coronavirus pandemic disrupted the lives and livelihoods of many people in 2020. COVID-19 impacted everything from education, food supply, health care to the job market and housing. In our evictions story, we look at how pressure on renters during the pandemic resulted in evictions and how layoffs contributed to an already unstable housing situation for many.

This repository shares the data about layoffs and closures in California from 2019-2020. Layoffs and closures have always been a consistent presence in the market place. For the purposes of our story, we analyzed the 2019 data and compared it to 2020 data, in order to assess the difference in job losses from a non-pandemic year to a pandemic year. 

For the purposes of this story, we've only done specific analyses on counties with high rent burdens and public housing authorities. There are many patterns present in this data we have yet to explore and we are sharing it with the hopes that other data journalists and news organizations will report similar stories of their own - and share their counties and cities have been impacted by layoffs and closures.


This data was used as a section in a larger evictions story written by Big Local News. 

The data was collected from:
- [California WARN data](https://edd.ca.gov/Jobs_and_Training/Layoff_Services_WARN.htm)
- [population data from](https://www.census.gov/data/tables/time-series/demo/popest/2010s-counties-total.html#par_textimage_242301767)
Add link for rent burden data

How to use this repository:

`processed_data.ipynb` and `rent_burden_calculation.ipynb` can be run simultaneously. The `processed` directory holds all WARN layoff records that were downloaded from the Employment Development Department. `processed_data.ipynb` creates a single file of all those records and exports it back to the `processed` directory.

`rent_burden_calculation.ipynb` takes ACS rent as a % of income data and the list of public housing authorities in California. With these two datasets, the rent burden in each county is calculated and merged with he public housing data, creating a table that shows the rent burden for the counties of each housing authority. This file is exported to the `rent_burden` directory as a full version with all of the columns and a truncated version with only the necessary columns.

Run the following notebooks in order:

1. `data_cleaning.ipynb`
2. `harmonize_dedupe.ipynb`
3. `warn_analysis.ipynb`

`data_cleaning.ipynb` cleans the data. Here, we get rid of white space and resolve conflicts between incorrect county names. Census population estimates are also read in and combined with the cleaned data. This file is exported to the `open_refine` directory. Update code so that there’s an open refine directory and it actually exports the file there.

The file is then manually cleaned in open refine. In this file, we detail the steps we took to standardize the data. This folder contains all of the changes made to our data via open refine.







 


