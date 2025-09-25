<h1>COVID-19 Impact on Retail Employment Analysis</h1>

<h2>Description</h2>
This project analyzes how the COVID-19 pandemic affected retail employment in the United States, using IPUMS CPS (Current Population Survey) microdata. The focus is on changes in total retail employment and average weekly hours worked before and after the onset of the pandemic in March 2020. By utilising R's Visualization and Statistical capabilities, this project aims to answer and display the impacts of COVID-19 on Retail relative to other industries and more!

<h2>Methods Used</h2>

1. R Libraries:
  - tidyverse – data wrangling and visualization
  - ipumsr – importing IPUMS CPS extracts
  - lubridate & zoo – handling dates and monthly time series
  - fixest – regression analysis (optional extensions)
2. Techniques:
  - Data cleaning & transformation pipelines
  - Weighted employment aggregation
  - Time-series visualization
  - Regression discontinuity design

<h2>Key Steps in Analysis</h2>

1. Data Cleaning
   - Filtered CPS data to include only retail industry codes.
   - Created pre- and post-COVID time markers.
   - Constructed weighted employment measures.
2. Exploratory Analysis
   - Plotted total retail employment trends over time.
   - Compared pre-COVID and post-COVID patterns.
   - Examined average weekly hours worked.
3. Causal Analysis
   - Applied Regression Discontinuity Design (RDD) around March 2020 to estimate COVID’s immediate effect.
  
<h2>Summarised Insights</h2>

- Retail employment showed a sharp jump/drop around March 2020, consistent with pandemic disruptions.

- Average weekly hours decreased post-COVID, reflecting reduced stability in retail jobs.

- RDD analysis highlights a structural break in retail labor dynamics at the onset of COVID.

- Greater in-depth insights offered inside [submission](https://github.com/a-paija/Covid-19-Retail-Employment/blob/main/Data%20Translation%20Submission.html)

<h2>Key Visualizations</h2>

![Retail](https://github.com/a-paija/Covid-19-Retail-Employment/blob/main/images/retail1.png)
![Retail](https://github.com/a-paija/Covid-19-Retail-Employment/blob/main/images/retail2.png)
![Retail](https://github.com/a-paija/Covid-19-Retail-Employment/blob/main/images/retail3.png)
![Retail](https://github.com/a-paija/Covid-19-Retail-Employment/blob/main/images/retail4.png)

<h2>Data Source</h2>

-IPUMS CPS (Current Population Survey): U.S. employment microdata (up to April 2022).

-Retail industries were selected using specific industry codes (motor vehicles, furniture, grocery, clothing, etc.).

<h2>Accessing the data</h2>

Open the Onedrive file and download the CPS_00002.xml and CPS_00002.dat files

NOTE: To load data, you must download both the extract's data and the DDI and also set the working directory to the folder with these files (or change the path below).

if (!require("ipumsr")) stop("Reading IPUMS data into R requires the ipumsr package. It can be installed using the following command: install.packages('ipumsr')")

ddi <- read_ipums_ddi("cps_00002.xml")

data <- read_ipums_micro(ddi)
