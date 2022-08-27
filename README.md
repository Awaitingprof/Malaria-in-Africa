# Malaria-in-Africa
This project focuses on the development of malaria in Africa during the past two decades and gives a thorough knowledge of that development (2007-2017).
In Africa, malaria is a widespread disease caused by mosquito bites and an untidy environment.It can be fatal even though it can be prevented by taking preventative measures. This dataset is gotten from kaggle. It contain all African countries from 2007 till 2017 as well as the unique country code, Latitude and Longitude of each country, and the preventive measure that have been taken to curtail Malaria in Africa. This project focuses on and provides a comprehensive understanding of how malaria has evolved in Africa over the last two decades (2007-2017).
 
 ## Methodology 
 Data Cleaning 
 Data Analysis
 Data Visualization 
 
 ### Data Cleaning 
 The dataset was downloaded in CSV(Comma Separated Values) format, and I converted it to excel format. The duplicated data was removed, and some special characters  were eliminated using find and replace in Full documentation is available at https://ebenezeradebiyi.wixsite.com/laconic-data/post/data-analysis-project-analysis-of-malaria-in-africa-from-2007-to-2017
 
 ### Data Analysis
 The dataset was imported into Sequel (SQL) and analysed. The codes are shown below.
 select * from [dbo].[Africa$]
 
/*  Total Country */

SELECT COUNT(DISTINCT Country) FROM [dbo].[Africa$] As Total_Country;

/* Total Malaria Case reported */

SELECT SUM(Malaria_reported) AS Total_Case_Reported FROM [dbo].[Africa$];

/* Trend in Malaria case reported over the year */

SELECT Year,SUM(Malaria_reported) As Total_Case_Reported FROM [dbo].[Africa$] GROUP BY Year Order BY Total_Case_Reported;

/* Total Malaria case reported in West Africa */

SELECT  SUM(Malaria_reported) AS Total_west_Africa FROM [dbo].[Africa$] WHERE Country IN ('Benin',  'Burkina Faso',  'Cape Verde',  'Cote Di voire', 'Gambia',  'Ghana', 'Guinea', 'Guinea_Bissau', 'Liberia',  'Mali',  'Mauritania',  'Niger',  'Nigeria', 'Senegal',  'sierra Leone',  'Togo');

/*  Trend in Malaria Case Reported Over the year in West Africa */

SELECT Year, SUM(Malaria_reported) AS West_Africa FROM WHERE Country IN ('Benin',  'Burkina Faso',  'Cape Verde',  'Cote Di voire', 'Gambia',  'Ghana', 'Guinea', 'Guinea_Bissau', 'Liberia',  'Mali',  'Mauritania',  'Niger',  'Nigeria', 'Senegal',  'sierra Leone',  'Togo') Group BY Year ORDER BY West Africa;

/* Total Malaria case reported in East Africa */

SELECT SUM(Malaria_reported) AS Total_East_Africa_Report FROM [dbo].[Africa$] WHERE Country IN ('Burundi', 'Comoros', 'Djibouti', 'Ethiopia', 'Eritrea', 'Kenya', 'Madagascar',  'Malawi',  'Mauritius',  'Mozambique',  'Rwanda',  'Seychelles', 'Somalia',  'Tanzania',  'Uganda');

/* Trend of Malaria case reported in East_Africa Over the year */

SELECT Year, SUM(Malaria_reported) AS East_Africa FROM [dbo].[Africa$] WHERE Country IN ('Burundi', 'Comoros', 'Djibouti', 'Ethiopia', 'Eritrea', 'Kenya', 'Madagascar',  'Malawi',  'Mauritius',  'Mozambique',  'Rwanda',  'Seychelles', 'Somalia',  'Tanzania',  'Uganda') GROUP BY Year ORDER BY East_Africa;

/* Total Malaria Case reported in South Africa */

SELECT SUM(Malaria_reported) AS Total_South_Africa_Report FROM [dbo].[Africa$] WHERE Country IN ('Angola', 'Botswana', 'Lesotho', 'Malawi', 'Mozambique',  'Namibia',  'South Africa',  'Zambia',  'Zimbabwe');

/* Trend in Malaria Case reported in South Africa Over the year */

SELECT Year, SUM(Malaria_reported) AS Total_South_Africa_Report FROM [dbo].[Africa$] WHERE Country IN ('Angola', 'Botswana', 'Lesotho', 'Malawi', 'Mozambique',  'Namibia',  'South Africa',  'Zambia',  'Zimbabwe') GROUP BY year ORDER BY Total_South_Africa_Report;

/* Total Malaria case reported in North Africa */

SELECT SUM(Malaria_Reported) AS Total_North_Africa_Report FROM [dbo].[Africa$] WHERE Country IN ('Algeria', 'Egypt', 'Libya',  'Morocco',  'Sudan',  'Tunisia');

/* Trend in Total Malaria case reported in North Africa over the year */
SELECT Year, SUM(Malaria_Reported) AS North_Africa FROM [dbo].[Africa$] WHERE Country IN  ('Algeria', 'Egypt', 'Libya', 'Morrocco',  'Sudan', 'Tunisia') GROUP BY Year ORDER BY North_Africa ;

/* Top 10 Country with malaria case reported */

SELECT Country, SUM(Malaria_Reported) AS Total_Case_Reported FROM [dbo].[Africa$] GROUP BY Country ORDER BY Total_Case_Reported DESC  10;
full documentation here :https://ebenezeradebiyi.wixsite.com/laconic-data/post/data-analysis-project-analysis-of-malaria-in-africa-from-2007-to-2017

### Data Visualization
The data was visualised with Tableau.
![dashboard Malaria](https://user-images.githubusercontent.com/102805397/187043805-d1bf8788-45ca-4276-85a3-69dedbc7d7db.PNG)
full documentation here: https://ebenezeradebiyi.wixsite.com/laconic-data/post/data-analysis-project-analysis-of-malaria-in-africa-from-2007-to-2017
