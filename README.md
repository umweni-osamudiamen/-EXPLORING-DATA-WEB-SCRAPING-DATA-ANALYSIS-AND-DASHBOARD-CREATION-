[Umweni_O_Capstone_project_2026.ipynb](https://github.com/user-attachments/files/24672990/Umweni_O_Capstone_project_2026.ipynb)
# EXPLORING DATA WEB SCRAPING DATA ANALYSIS AND DASHBOARD CREATION

# Objective:

The global topic or trend for decades now has been centred around population growth management due to its relevance in many aspects of human existence like security, food & agriculture, housing and many more. So, the need for census and population management is very important in a time like this. In this project I will be scraping 2025 world population data from Wikipedia, a publicly accessible website.
# Introduction:

The term population refers to a community or a group of animals or persons living or occupying a particular location, and the total number of persons in a place. So “World population 2025” refers to the total number of persons living in the world in the year 2025, but for this project and to enable an in-depth analysis, data regarding fertility rate, population density, land area, urban percentage population, world share and many more will be analyses alongside the population 2025.

In this project, I scraped data from

url = ("https://www.worldometers.info/world-population/population-by-country/") using Python.

The procedure followed includes:
Identifying the website to scrape, so after identifying this

from bs4 import BeautifulSoup
import requests

url = "https://www.worldometers.info/world-population/population-by-country/"

headers = {
"User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) "
"AppleWebKit/537.36 (KHTML, like Gecko) "
"Chrome/120.0.0.0 Safari/537.36",
"Accept-Language": "en-US,en;q=0.9",
}

page = requests.get(url, headers=headers)

soup = BeautifulSoup(page.text, "html.parser")

I added headers so python can identify and pass the url

print(soup)

This world population is a topic of choice because of its relevance to trends, trade, governance, policy formation, and security, among others. It is a global concern for world leaders because it affect migration and in some cases de-stabilizes processes.

# Data Cleaning:

<img width="1352" height="438" alt="raw data" src="https://github.com/user-attachments/assets/e5390cd1-31d9-44d7-8f23-a59287c43cee" />
#Raw Data

#Objective:
The data set scraped using python was saved in csv format as seen below, it was then imported into panda’s environment for cleaning. The objective of cleaning the dataset was to make clean, free of inconsistent, misplace, incorrect, and unaligned datapoints that will in one way or the other interfere with the analysis outcome.
Missing Data: Based on it being a public data some missing data point were researched and replaced.
Remove Duplicates: There are no duplicates.
Format Data: The data format in the units were corrected
Inconsistencies: The inconsistent data found in heading like in Fert. Rate, Country (or dependency), Density (P/KmÃ‚Â²), Ã¢ÂˆÂ’495,753 as seen in the image below were all clean using pandas;

<img width="1340" height="460" alt="cleaned data" src="https://github.com/user-attachments/assets/4f9ca823-22c8-4114-b3bf-cb56ca263d39" />
# Cleaned Data

The outcome of the data after cleaning are presented below

# Pre-Analysis
# Data Split:

Dependent data: Density, Fertility Rate, Net Change, Net Migrants, Population 2025, Urban population, World share, Yearly Change, Median Age

Independent data: Country, Serial Number, Land Area

Industry: Population Department

Story of data:
This data is a secondary dataset that describes the compilation of the world population data for 2025, and it comprises 233 countries cutting across different continents of the world of various sizes. It gives details like Fertility Rate, Net Change, Net Migrants, Population 2025, Urban population, World share, Yearly Change, Median Age, among others.

Stakeholders:
Governments of Nations, Chief executive officers, United Nations, World Health Organisation, International Monetary Fund, etc.

# Potential Analysis Questions
1. Determine the total world population in 2025.
2. What is the possible average median age?
3. What is the average land area?
4. What is the yearly population change by Country?
5. What is the fertility rate by Country?
6. What is the urban population ratio?
7. What is the population share for 2025 by countries of the world
   
# Potential Analysis Insights
1. Sum of population 2025
2. The average median population by country can be determined
3. Land area covered by population
4. The rate of population growth by delivery per country
5. Urban population contribution to the total population
6. The share of the total population is taken by each country
7. The mean net population change

<img width="615" height="351" alt="pre-analysis" src="https://github.com/user-attachments/assets/284b02b1-87a1-4a74-9613-2db8dc3dfca6" />


# Exploratory Data Analysis:
This analysis helps in getting a summarized view of the analysis process and outcome.
The exploratory analysis was carried out by creating new measures to calculate mean, median, average respectively.

# Method:
Right click on data set and create new measure
Then name and appended the new measure for average, sum and mean.
Average_Population = AVERAGE(Cleaned_world_population_data[Population 2025]) Count_of_Countries = COUNT(Cleaned_world_population_data[Country]) Mean_Net_Change = GEOMEAN(Cleaned_world_population_data[Net Change]) Sum_of_Population_2025 = SUM(Cleaned_world_population_data[Population 2025])

<img width="882" height="468" alt="card" src="https://github.com/user-attachments/assets/a5138973-abe2-4bd2-ac44-7c886f023482" />
# Cards
The outcome this process was converted into card for visuals

# Visualizations:
Visualizations carried includes plotting a bar chart, heat map, funnel chart, column chart, table, cards and many others. In certain conditions for card new measures were used to calculate the value before visualizing them.

<img width="882" height="468" alt="card" src="https://github.com/user-attachments/assets/8e014e41-0096-430d-8aa1-b5e8e5d15e0b" />
# Cards:
Cards were used to buttress additional information that the charts give, like the card average give more information about the average population size in total, average population density, cards were used to visualize mean net change, average fertility rate, sum of population and count of countries in the dataset.

Column Chart:
This was used to visualize the fertility rates against the countries before filtering the top 5 most fertile countries.
<img width="811" height="407" alt="Fertility Rate" src="https://github.com/user-attachments/assets/5bb9c58a-ef2a-4b9d-a67d-3728b41be37d" />

<img width="355" height="240" alt="median age" src="https://github.com/user-attachments/assets/b2d60758-78b0-43db-9d4d-d1f3fbe9103e" />
Dough Nut Chart:
This chart was used to visualize the median age by countries there by revealing the percentage of middle or median individual or citizen per country.

<img width="480" height="401" alt="migrant population" src="https://github.com/user-attachments/assets/ae05d30d-bcaf-48d4-b384-f873a18c974a" />

# Funnel Chart:
Net migrants population which reveal the rate at which people go in and out of the country.

<img width="686" height="390" alt="population density" src="https://github.com/user-attachments/assets/9ed010a0-f1eb-4ced-8042-0eb96c47da14" />

# Bar Chart:
Bar Chart in this project was used to visualize the population density in Km square, which tells us how dense the population is.

<img width="787" height="464" alt="Urban Population" src="https://github.com/user-attachments/assets/3562e3b5-d111-43b1-8819-fe0963651d5c" />

# Pie Chart:
The percentage of the population contributed by the urban population is represented here.

<img width="633" height="413" alt="yearly change by population 2025" src="https://github.com/user-attachments/assets/286a791e-f7fb-4f9a-8792-91c9351e0a77" />
# Line Chart:
The line chart displays the rate at which the population of each country changes, and indirectly telling how the world population changes.

# Dashboard:
The Dashboard displayed below shows interactive visuals of different visuals combined. It contains two slices which are used for filtering the dashboard.
It has a navigation card that allows a quick transition from one page to another.
It has sets of cards that were used to pinpoint certain key metrics like sum of population 2025.
The chart was used to summarise the data sets for more insights.
<img width="516" height="513" alt="DASHBOARD JOINED" src="https://github.com/user-attachments/assets/ebc147ee-f063-46bc-9833-72e2067b7bdf" />

<img width="1099" height="547" alt="Main Dashboard" src="https://github.com/user-attachments/assets/752c6ec8-4d10-4cb0-bb14-16e058408c0a" />

<img width="1099" height="547" alt="Main Dashboard" src="https://github.com/user-attachments/assets/8d4182e1-f886-4db9-a420-7d86075afc15" />

# In - Analysis Observation
1. 0.041 means Tokelau has a greater yearly change in population than other countries. Angola, with 0.031, is the last of the top 10 by yearly change in population.
2. Sint Maarten Urban population contributes 20.31% of the total urban population, Belgium 20.1%, and the least is 19.74%.
3. In terms of fertility rate, Chad is the most fertile country by population at the rate of 5.94, followed by Somalia, DR Congo, the Central African Republic and then Niger to complete the top 5.
4. Holy See has a median age of 57.4 as it sum, and it is the highest of all the countries.
5. Ukraine's migrant population was 1.7M as of 2025, the United States 1.23M, Syria 0.42M, the United Kingdom 0.39M and Canada 0.33M.
6. Monaco has the largest population per square metre, 25.7K, followed by Mecao while Gibraltar is the least, by square metre 4.0K.

<img width="506" height="463" alt="Observation" src="https://github.com/user-attachments/assets/b34579be-be8a-493d-b383-cbc7f9b3d13c" />


# In - Analysis Recommendations
1.For the top 10 countries by population yearly change, they should look into factor that may be responsible for such yearly increase in context
2. Sint Maarten should consider dicentralising their population across urban and rural areas to avoid urban congestion.
3. A country like Chad, withthe highest fertility rate, can consider birth rate reduction
4. The median age should be compared withthe active workers' age to know the country's workforce
5. The migrant population is highest in Ukraine, the USA, and Syria, so ensure proper documentation to safeguard the Cities.
6. Monaco should diversify into new areas to accommondate for the growing population.
Analysis Observations
1. From observations United States have 347.28M population as average, covering an average of 9.15M sqm in land area. Mean net change is 1.85M people with a median population of 347.28M people. United States has a population change of 0.005 annually, fertility rate of 1.62, and average population density of 38 people per square area. The net migrant’s population for United States is 1.23M people.
2. Following careful observation Pakistan had a mean net change of 3.95M followed by a 255.22M average population, 20.6 median population, and sum of population was at 255.22M. Average land area is 770.88K, urban population 100% with a fertility rate of 3.50. The net migrants population for Pakistan clocked -1.24M.
3. Observations reveal that the values for population where not only at high in United States and Pakistan but was at reasonably high in Indonesia too with a sum of population of 2.857M people make it the 3rd largest population after indian and China.
4. It has an average population density of 158, average land area of 1.81M, fertility rate of 2.1 per populace. The net migrants population was at -39.51K, and the bulk of the population was dominated by the middle age group from observations. Yearly population change was 0.008, mean net change 2.23M.
5. Visual observations reveal that China has a yearly population change of -0.002, mean net change was at -3.23M, with a total population sum of 1416.10M, and population density of 151p/km square. Urban population was represented at a 100 percent, average land area of 9.39M, net migrants population was -268.13K fertility rate of 1.02 in China.
6. India from observations is the world largest country by population ii n 2025, with a population sum of 1463.87M people giving an approximated figure of about 1.4B people, and population density was at 492, mean net change 12.93M, fertility rate stands at 1.94, and average land area is 2.97M. It is important to note that most of this population is found in the urban area.

<img width="506" height="463" alt="Observation" src="https://github.com/user-attachments/assets/2b16208c-d057-446c-a1ff-7e52a4cdcf75" />


# Analysis Recommendations
1. Governments of nations within the top 10 largest countries by population should ensure a strict policy on child birth, and pregnancy.
2. Governments, agencies, and other policy formulators must ensure continuous promotion of contraceptives benefits, methods, and availability, and cost effectiveness
3. Governments and developers must ensure new infrastructures are built in rural areas and urban areas to accommodate the constantly increasing population.
4. Public enlightenment and education must be carried out deliberately to sensitize citizens on the need to curb excessive population growth.
5. Countries with a high migrant population will need to review immigration laws to curb illegal migration.
6. Urban area managers should enact laws that will help decongest it.
7. Rural development should be encouraged across board to avoid over congestion in urban areas.
<img width="1099" height="547" alt="Main Dashboard" src="https://github.com/user-attachments/assets/f33f742d-e442-4611-994b-fe60481872d7" />


Conclusion:
From the analysis it was clear that the three most populated countries in the world are India 1,463,865,525, China 1,416,096,094, and the United States with the latter having the least population of about 347,275,807 people. Also uncovered was that these countries have high fertility rates, making population growth by birth a major issue, the United States had more and a positive migrant value of 1230663, there was a need for immigration agencies to address its regulations. For future analysis more data set across different years should be used, and other details like number of births per year, death rate, and rural settlers’ percentage should be included.
[Umweni_O_Capstone_project_2026.ipynb](https://github.com/user-attachments/files/24672997/Umweni_O_Capstone_project_2026.ipynb)
[Umweni_O_Capstone_project_2026.ipynb](https://github.com/user-attachments/files/24673010/Umweni_O_Capstone_project_2026.ipynb)
