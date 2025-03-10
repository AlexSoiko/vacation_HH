# vacation_HH
Настоящий проект посвящен анализу вакансий в HeadHunter с помощью SQL запросов. 
## Проект включает в себя несколько этапов:
1. Знакомство с данными
2. Предварительный анализ данных
3. Детальный анализ вакансий
4. Анализ работодателей
5. Предметный анализ

## 1. Знакомство с данными:
Все необходимые таблицы находятся в схеме public базы данных project_sql (именно эту база указана в параметре dbname при подключении).
Параметры подключения:
DBNAME = 'project_sql'
USER = 'skillfactory'
PASSWORD = 'cCkxxLVrDE8EbvjueeMedPKt'
HOST = '84.201.134.129'
PORT = 5432

## 2. Предварительный анализ данных:
В процессе предварительного анализа данных общее количество:
1) вакансий в базе (vacancies) составляет 49197
2) работодателей в базе (employers) насчитывается 23501
3) регионов в базе (areas) достигает 1362
4) сфер деятельности в базе (industries) значится 294

## 3. Детальный анализ вакансий:
1) определена пятерка "лидеров" по числу вакансий в базе. Наибольшее количество вакансий в Москве 5333 вакансий;
2) установлено, у какого количества вакансий заполнено хотя бы одно из двух полей с зарплатой, их в базе 24073;
3) известны средние значения для нижней (71065.0) и верхней границы (110537) зарплатной вилки;
4) выяснено количество вакансий для каждого сочетания типа рабочего графика (schedule) и типа трудоустройства (employment), используемого в вакансиях, данные отсортированы по убыванию количества (Полный день/Полная занятость). Установлено 35367 вакансий, сочетающих работу на полный день с полной занятостью;
5) определен требуемый опыт работы в порядке возрастания по количеству вакансий, самый востребованый опыт от 1 года до 3 лет.

## 4. Анализ работодателей:
1) определены, какие работодатели находятся на первом(Яндекс) и пятом(Газпром нефть) месте по количеству вакансий;
2) база не позволяет установить перечень регионов, среди которых нет вакансий, установлено 410 работодателей в России, у которых нет вакансий;
3) для каждого работодателя определены количество регионов, в которых он публикует свои вакансии: "Яндекс" (181), "Ростелеком" (152), "Тинькофф" (43), "СБЕР" и "Газпром нефть" по (24).
4) у 8419 работодателей не указана сфера деятельности;
5) компания "2ГИС" на третьем месте в алфавитном списке, у которой указано четыре сферы деятельности;
6) установлено 3553 работатодателя, в сфере деятельности которой указана Разработка программного обеспечени;
7) для компании «Яндекс» установлен список регионов-миллионников, в которых представлены вакансии компании и количеством вакансий в них. В строке Total 485 общее количеством вакансий компании в городах-миллионниках.

## 5. Предметный анализ:
1) количество вакансий, имеющим отношение к данным (со слова 'data' или 'данн') составляет 1771;
2) для начинающего дата-сайентиста в базе представлена 51 вакансия;
3) 229 вакансий для DS, в которых в качестве ключевого навыка указан SQL или postgres;
4) представлено 357 вакансий на HeadHunter, к которым предъявляются требования работателей по знанию Python;
5) в среднем 6,41 ключевых навыков указывают в вакансиях для DS;
6 установлено, что дата-сайентист с опытом работы от 3 до 6 лет в среднем может рассчитывать на зарплату 243115.00.

На первый взгляд, анализ показал, ято вакансий связанных с Data Science не так много относительно всех данных представленных в таблице, в основном наибольшее число запросов в городах-миллионниках (Мосва, Санкт-Петербург и др.). Наибольшее количество вакансий представлено "Яндекс", "Ростелеком", банками. Высокая средняя зарплата, относительно небольшое среднее число ключевых навыков, необходимых для работы. Новичкам сложнее найти работу в сфере DS. Для предсказания модели желаемой заработанной платы, необходимо очистить данные, провести разведовательный анализ.
