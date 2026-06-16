PROJECT- Summative:Freeform Programming Exercise 

Project description:
Exploring worldwide measles and rubella cases between 2012-2025.
Seven different graphs were created to answer the following questions.
Scored a high merit grade.

1. How has global measles and rubella cases changed over time?
2. How does measles and rubella cases vary by region?
3. How does measles diagnosis vary by region?
4. Are there seasonal variations in measles cases?
5. Which countries have the highest measles cases?
6. Which countries have high measles incidence rates?
7. Does a higher percentage of vaccine coverage result in lower measles incidence?

==================================================================================================================================
CODE

Python packages required:
Pandas
Matplotlib 
Seaborn 
Plotly.express
NumPy 

CODE description:
The code (measles_code.ipynb) was written using a Jupyter lab notebook. 

The notebook and code is divided into eight main sections. 

Section 1
The first section of the code installs the packages required, and loads the dataset cases_year.csv which 
was used to create the first five figures.

Section 2
The code creates Fig1.png- a line plot of global cases between 2012-2025.
The data is grouped by year to get the sum of measles, rubella and total suspected measles and rubella cases for 
each year globally.

Section 3
The code creates Fig2.png- a stacked bar plot showing the number of suspected measles and rubella cases yearly by region
Each bar represents the total number of suspected measles and rubella cases each year between 2012-2025
The different stacks within the bars represent the number of cases in each WHO region.

Section 4
The code creates Fig3.png- a stacked bar plot showing the average number of measles cases in each WHO region
Each bar represents the average number of measles cases between 2012-2025 in each region
The different stacks within the bars represent the average number of measles cases by measles diagnosis method

Section 5
The code creates Fig4.png- a choropleth showing the average measles cases between 2012-2025 by country

Section 6
The code creates Fig5.png- a bar plot of the top ten countries with the highest measles incidence rate in 2024

Section 7
The code creates Fig6.png- a line plot of the average number of measles cases per month for each region 
The dataset cases_month.csv was loaded and used to create the figure. 

Section 8
The code creates Fig7.png- a scatter plot depicting the relationship between vaccination coverage(%) and measles incidence rate 
The dataset measles_vaccination.csv was used to obtain vaccination coverage by year for each region. 
Measles incidence rate per million was calculated for each region using population and measles cases columns from cases_year.csv data. 

=========================================================================================================================================
DATASETS 

1.FILE: cases_year.csv 

Downloaded from tidytuesday: https://github.com/rfordatascience/tidytuesday/blob/main/data/2025/2025-06-24/cases_year.csv
Date of download: 06/01/2026

Dataset description
Consisted of yearly measles and rubella data for each country between 2012-2025.
Each row represents a country with the following information.

VARIABLES                                                               DESCRIPTION 
region (String                                                         | region code
country (String)                                                       | country name
iso3 (String)                                                          | three letter country code
year (Int)                                                             | year 
total_population (Int)                                                 | country population
annualized_population_most_recent_year_only (Int)                      | annualized population 2025
total_suspected_measles_rubella_cases (float)                          | suspected number of measles and rubella cases in country
measles_total (Int)                                                    | lab + epi + clinical measles cases in country
measles_lab_confirmed (Int)                                            | lab confirmed cases in country
measles_epi_linked (Int)                                               | epidemiologically-linked measles cases in country
measles_clinical (Int)                                                 | clinically confirmed cases in country
measles_incidence_rate_per_1000000_total_population                    | measles cases per million population 
rubella_total (Int)                                                    | lab + epi + clinical rubella cases in country
rubella_lab_confirmed (Int)                                            | lab confirmed cases in country
rubella_epi_linked (Int)                                               | epidemiologically linked cases in country
rubella_clinical (Int)                                                 | clinically confirmed cases in country         
rubella_incidence_rate_per_1000000_total_population (float)            | rubella cases per million population
discarded_cases (float)                                                | suspected case that has been investigated and discarded (measles and rubella) in country
discarded_non_measles_rubella_cases_per_100000_total_population(float) | discarded cases per million population


2.FIEL: cases_month.csv 

Downloaded from tidytuesday: https://github.com/rfordatascience/tidytuesday/blob/main/data/2025/2025-06-24/cases_month.csv
Date of download: 06/01/2026

Dataset description
Consisted of monthly measles and rubella data for each year between 2012-2025 for all countries
Each row represents a country with the following information.

VARIABLES                                                       DESCRIPTION 
region (string)                                                 | region code
country (string)                                                | country name
iso3 (string)                                                   | three letter country code
year (int)                                                      | year 
month (int)                                                     | month
measles_suspect (float)                                         | suspected number of measles in country
measles_clinical (float)                                        | clinically confirmed cases in country 
measles_epi_linked (float)                                      | epidemiologically-linked measles cases in country
measles_lab_confirmed (float)                                   | lab confirmed cases in the country
measles_total (float)                                           | lab + epi + clinical measles cases in country
rubella_clinical (float)                                        | clinically confirmed cases in country
rubella_epi_linked  (float)                                     | epidemiologically linked cases in country
rubella_lab_confirmed (float)                                   | lab confirmed cases in country
rubella_total  (float)                                          | lab + epi + clinical rubella cases in country
discarded_cases (float)                                         | suspected case that has been investigated and discarded (measles and rubella)

3. FILE: measles_vaccination.csv

Downloaded from WHO website: https://immunizationdata.who.int/global/wiise-detail-page/measles-vaccination-coverage?GROUP=WHO_REGIONS&ANTIGEN=MCV2&YEAR=&CODE=
Date of download: 06/01/2026

Dataset description
Consisted of antigen used, number of doses administered and vaccine coverage (%) for each WHO region between 2012-2024.
Each row represents a WHO region with the following information.

VARIABLES:                             Description
GROUP (string)                         | indicates data was grouped by WHO region
CODE  (string)                         | three letter WHO region code
NAME  (string)                         | name of WHO region 
YEAR  (float)                          | year
ANTIGEN (string)                       | antigen administered 
ANTIGEN_DESCRIPTION (string)           | description of antigen 
COVERAGE_CATEGORY (string)             | coverage category 
COVERAGE_CATEGORY_DESCRIPTION (string) | coverage category description 
TAREGT_NUMBER (float)                  | target number of doses to administer               
DOSES (float)                          | doses administered 
COVERAGE (float)                       | percent of eligible population vaccinated
