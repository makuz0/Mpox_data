__Data:__
This dataset contains information on monkeypox cases and deaths in various locations from May 2022 to May 2023. The data includes 33,666 rows and 15 columns, with each row representing a unique combination of location, date, and corresponding monkeypox cases and deaths.
The dataset is taken from Kaggle from the Our World in Data project and does not contain missing values.

*location* - name of the place (continent or country)

*iso_code* - location code

*date* - date of observation

*total_cases* - the total number of cases of monkeypox reported in a given area up to this date

*total_deaths* - the total number of deaths from monkeypox recorded in a given area up to this date

*new_cases* - number of new cases of monkeypox registered on the observation date

*new_deaths* - number of new deaths from monkeypox recorded on the observation date

*new_cases_smoothed* - 7-day smoothed average number of new cases of monkeypox reported on the observation date

*new_deaths_smoothed* - 7-day smoothed average of new monkeypox deaths reported to date of observation

*new_cases_per_million* - number of new cases of monkeypox recorded per million population on the date of observation

*total_cases_per_million* - Total number of reported cases of monkeypox per million population up to the observation date

*new_cases_smoothed_per_million* - 7-day smoothed average number of new monkeypox cases reported per million population per observation day

*new_deaths_per_million* - number of new deaths from monkeypox recorded per million population on the observation date

*total_deaths_per_million* - total number of deaths from monkeypox recorded per million population up to the observation date

*new_deaths_smoothed_per_million* - 7-day smoothed average number of new monkeypox deaths reported per million population on the date of observation

__Tasks:__
1. In which country did the first case of infection occur, on what date?
2. In which country did the first death occur, on what date?
3. Percentage of cases/deaths by country?
4. Mortality rates by country?
5. Determining trends in infection and mortality?
6. Plotting a graph of the growth of cases and deaths by country?
7. Visualization on the map of infected countries and the number of deaths?

__Stack:__
Python
pandas
plotly.express
matplotlib.pyplot
geopandas

__Results:__

0. Data preparation and verification
1. It was revealed that all countries sorted by the minimum date and the presence of cases of illness and death belong to the continent of Africa (Cameroon, Central African Republic, Congo, Ghana, Nigeria). Therefore, we conclude that the disease was first identified in Africa. The first cases of Mpox were recorded on 2022-05-01 in Africa. 27 cases of the disease were identified.
2. The first deaths occurred on 2022-05-01 in: Cameroon, Nigeria, 2 people died there.
3. Based on the data obtained, we can conclude that almost a third of cases and deaths occur in the United States. And the first seven countries (United States, Brazil, Spain, France, Colombia, Mexico, Peru) account for ~75% of all cases and deaths.
Most countries are located in the Americas, although the first cases of infection were in Africa, where the population is about 1.4 billion people, which is 1.5 times the combined population of the Americas. Such results may be obtained due to differences in the level of medicine and the number of tests performed. The percentage of infection in other countries with a large population is also extremely low, which may indicate a weak spread of the virus or a lack of “universal” testing.
4. The mortality rate does not exceed one percent, and the average mortality rate is 0.18%, which is almost equal to the mortality rate from influenza in the world (0.01-0.2%). It is important to note that mortality in more developed countries tends to zero. We can conclude that monkeypox is not as dangerous as previously stated. Top 5 countries by mortality: Nigeria(0.98%), Mexico(0.65%), Ecuador(0.56%), Peru(0.53%), Belgium(0.25%)
5. According to the graph, it is clear that the spread of the virus is declining, since the number of cases is decreasing, but the number of deaths is increasing, this could indicate an increase in the aggressiveness of the virus, but taking into account the incubation period and duration of the disease (in total it can take up to one and a half months), apparently, these are the results of previous peaks of the disease and additional testing and recording of monkeypox deaths. I believe that based on the available data, monkeypox is on the decline and will not reach the level of development similar to CoVID-19.
6. Implementation using Tableau
7. Prepared an interactive map with visualization of countries with the presence of Mpox infection and deaths.
