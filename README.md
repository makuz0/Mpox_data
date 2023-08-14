__Данные:__
Этот набор данных содержит информацию о случаях заболевания обезьяньей оспой и смертельных исходах в различных местах с мая 2022 года по май 2023 года. Данные включают 33 666 строк и 15 столбцов, причем каждая строка представляет собой уникальную комбинацию местоположения, даты и соответствующих случаев заболевания обезьяньей оспой и смертей.
Набор данных взят из Kaggle из проекта "Our World in Data" и не содержит пропущенных значений.

*location* - название места (континент или страна)

*iso_code* - код местоположения

*date* - дата наблюдения

*total_cases* - общее количество случаев заболевания обезьяньей оспой, зарегистрированных в данной местности до этой даты

*total_deaths* - общее количество смертей от оспы обезьян, зарегистрированных в данной местности до этой даты

*new_cases* - количество новых случаев заболевания обезьяньей оспой, зарегистрированных на дату наблюдения

*new_deaths* - число новых случаев смерти от оспы обезьян, зарегистрированных на дату наблюдения

*new_cases_smoothed* - 7-дневное сглаженное среднее число новых случаев заболевания обезьяньей оспой, зарегистрированных на дату наблюдения

*new_deaths_smoothed* - 7-дневное сглаженное среднее значение новых случаев смерти от оспы обезьян, зарегистрированных на дату наблюдения

*new_cases_per_million* - число новых случаев заболевания обезьяньей оспой, зарегистрированных на миллион населения на дату наблюдения

*total_cases_per_million* - Общее число зарегистрированных случаев заболевания обезьяньей оспой на миллион населения до даты наблюдения

*new_cases_smoothed_per_million* - 7-дневное сглаженное среднее число новых случаев заболевания обезьяньей оспой, зарегистрированных на миллион населения в день наблюдения

*new_deaths_per_million* - число новых случаев смерти от оспы обезьян, зарегистрированных на миллион населения на дату наблюдения

*total_deaths_per_million* - общее число смертей от оспы обезьян, зарегистрированных на миллион населения до даты наблюдения

*new_deaths_smoothed_per_million* - 7-дневное сглаженное среднее число новых случаев смерти от оспы обезьян, зарегистрированных на миллион населения на дату наблюдения

__Задачи:__
1. В какой стране произошел первый случай заражения, в какую дату?
2. В какой стране произошел первый случай смерти, в какую дату?
3. Процент заболевших/умерших по странам?
4. Смертность по странам?
5. Определение тенденции распространения инфекции и смертности?
6. Построение графика роста заболевших и умерших по странам?
7. Визуализация на карте зараженных стран и кол-во умерших?

__Стек:__
Python
pandas
plotly.express
matplotlib.pyplot
geopandas

__Результаты:__
0. Подготовка и проверка данных
1. Выявлено, что все страны, отсортированные по минимальной дате и наличием случаев заболевания и смерти относятся к континенту Africa (Cameroon, Central African Republic, Congo, Ghana, Nigeria). Поэтому делаем вывод, что впервые заболевание было выявлено в Африке. Первые случаи Mpox зафиксированы 2022-05-01 в Africa. Было выявлено 27 случаев заболевания.
2. Первые случае смерти произошли 2022-05-01 в: Cameroon, Nigeria, там умерло 2 человека.
3. На основании полученных данных можно сделать вывод, что практически треть случаев заболевания и смертей приходится на США. А на первые семь стран (United States, Brazil, Spain, France, Colombia, Mexico, Peru) приходится ~ 75% всех случаев заболевания и смертей.
Большинство стран располагается в Северной и Южной Америки, хотя первые случае заражения были в Африке, где население составляет порядка 1,4 млрд. человек, что в 1,5 раза превышает совокупное население Северной и Южной Америки. Такие результаты могут быть получены по причине различия уровня медицины и кол-ве проводимых тестах. Также крайне мал процент заражения в других странах с большим кол-вом населения, что может говорить о слабом распространении вируса, либо отсутствием "поголовного" тестирования.
4. Смертность не превышает одного процента, а средний процент смертности равен 0.18%, что практически равносильно смертности от гриппа в мире (0,01-0,2%). Важно заметить, что смертность в более развитых странах стремится к нулю. Можно сделать вывод, что обезьянья оспа не так опасна, как об этом заявлялось ранее. Первые 5 стран по смертности: Nigeria(0.98%), Mexico(0.65%), Ecuador(0.56%), Peru(0.53%), Belgium(0.25%)
5. Согласно данным графика видно, что распространение вируса идёт на спад, так как кол-во случаев снижается, однако кол-во смертей увеличивается, это могло бы говорить об увеличении агрессивности вируса, но учитывая инкубационный период и длительность болезни (в сумме может занимать до полутора месяцев), по всей видимости, это результаты предшествующих пиков заболевания и дополнительное тестирование и учет умерших от оспы обезьян. Считаю, что на основании имеющихся данных, оспа обезьян идёт на спад и не достигнет развития подобного CoVID-19.
6. Реализация при помощи Tableau
7. Подготовил интерактивную карту с визуализацией стран с наличием инфекции Mpox и смертям.
