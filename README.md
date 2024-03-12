# Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors
Studying about nations, age, gender, generations to look for trends and possible factors that are a reason for suicides using Tableau.



Visualizing Suicide Trends: Exploring Patterns and Influencing Factors

Introduction:
Millions of people worldwide endure trauma by committing suicide, which is a grave public health concern. Making successful preventive plans and support systems requires first understanding suicide patterns and then figuring out potential contributing factors. The goal of this data visualization project is to investigate global patterns in suicide using interactive visualizations. We'll examine suicide rates across nations, age, genders, and generations to look for trends and possible influencing variables.
Dataset:
The Dataset I have chosen for this project is “SuicideData” from Kaggle ( https://www.kaggle.com/datasets/data855/sucidedata ) this file contains only one csv file naming SuicideData.csv and this csv file has 12 columns in total.
Attributes:
Total of 12 attributes are there in this dataset, they are:
1.	country: Name of the Country where the suicide took place.
2.	year: Year in which the suicide took place.
3.	sex: The gender of the person.
4.	age: Age of the person.
5.	suicide_no: The number of suicides recorded for that gender, age respectively.
6.	population: number of suicides for a particular country, year, gender, and age group.
7.	suicides/100k pop: number of suicides per 100,000 people for a specific nation, year, sex, and age group combination.
8.	country-year: Name of the country and year in single column.
9.	HDI for year: Human Development Index (HDI) for that particular year.
10.	gdp_for_year: Represents the nation's Gross Domestic Product (GDP) for that particular year.
11.	gdp_per_capita: represents the nation's GDP per person for the given year, showing the population's level of economic prosperity.
12.	generation: Generation to which the person belongs to. Total 6 types of generations are there total, they are:
•	Silent: 1928-1945
•	Boomers: 1946-1964
•	Generation X: 1965-1980
•	Millennials: 1981-1996
•	Generation Z: 1997-2012
•	G.I Generation: 1901-1927

Tools used:
Tableau
Python

Exploratory Data Analysis:
First, I imported the dataset using pandas and then I checked for any missing values present.
I have displayed the data.

![WhatsApp Image 2024-03-12 at 1 55 16 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/43bbaf7d-bb57-499d-b8fa-decb70cc6fb6)
head(): This function displays first 5 rows of the data.

![WhatsApp Image 2024-03-12 at 1 55 31 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/0b2ca032-f358-4a26-b0ef-43cc0de8bfd7)
Info(): Prints information about the data frame.
 
![WhatsApp Image 2024-03-12 at 1 56 08 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/4229bb32-fdfd-41cc-bd81-691b2f48eb81)
The overview of attributes:
Describe(): this function is used to calculate statistical fields like mean, standard deviation and more.
 ![WhatsApp Image 2024-03-12 at 1 56 16 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/3e8e7863-dd17-4b95-97e2-1b9b854328e2)
Isnull(): to check for null values.

![WhatsApp Image 2024-03-12 at 1 56 24 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/b003975a-1548-4a88-a7f0-7022671aa010)
 
Total we have 27820 rows in this dataset, and the missing values for HDI has 19456 which is huge high, so I plan to remove this so that it won’t mislead the visualization.
Data Cleaning: 

![WhatsApp Image 2024-03-12 at 1 56 34 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/b77ec251-c7ed-46ff-8822-1815123e3f5f)

Correlation Matrix:
Correlation matrix is used to know about how strong the relation between the two variables is, the positive values represent the positive correlation and negative values represent the negative correlation.
 
![WhatsApp Image 2024-03-12 at 1 56 40 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/a87f26a4-9a22-4576-862d-7f2ce7c22c58)

![WhatsApp Image 2024-03-12 at 1 56 46 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/c8a456b6-7b18-4a59-a39e-89f4d738a603) 

Hypothesis (using python):

1.	Which age group has the highest suicide rates?
  
![WhatsApp Image 2024-03-12 at 1 56 55 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/3862af4e-315f-493a-bb3b-85e304be5d76)

Result: From the above graph, more suicide rates happed with who were above 75 and above years.

2.	Is there any relation between gdp_per_Capita and suicide/100k pop? 
 
![WhatsApp Image 2024-03-12 at 1 57 02 PM](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/19ba9472-54dc-4c2d-b756-203158bfe481)


Result: From the above graph we can conclude that there is a negative relation between gdp per capita and suicide rate/ 100 that is if GDP per capita increases then suicide rate tend to decrease.


Hypothesis(using tableau):
•	What is the number of each country suffering from suicide rate. Is there any increase in the suicide rates in given time?
•	Analyze whether gender plays a role. How has this changed over a given period?
•	Understanding the Impact of Generation on Suicide Rates. How do suicide rates differ across different generations? Is there any generational pattern in suicide rates, and how has it changed over the years?
•	Top 5 highest and lowest suicide rate country.

3.	 What is the number of each country suffering from suicide rate.
Map:
I have used a Map to answer this question, double click on the country and have labeled both year and suicide 100k/pop. And I have added year and sex as the filter so that we check for respective year and gender.

![Sheet 1](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/9e2f7a33-6a32-401e-a2dd-7356f66b0e46)
 
Result: From this map it is easy to check the suicide number by changing the year at filter section also we can do this based on the gender as well. The darkest color represents the high value and the lighter represent the low value. 
Is there any increase in the suicide rates in given time?
Line Graph:
To plot this information, I have used a line plot, as all the ups and down should be displayed clearly. Drag year to columns and suicide/100k pop to rows, I have used sex and gender as filter. Also, Suicide/100k pop to color.
![Sheet 2](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/e21af58b-d734-44d4-96de-29f89ee1f2ab)
 
Result: From the graph, it’s clear that there is an increase in suicide with increase in population over years till 2000 but it had decreased from 2000 to 2018 and this increase and decrease is not a straight line, and we can filter this based on the generation and check that for each generation.

4.	Analyze whether gender plays a role. 
Bar plot:
To achieve this bar plot I have droped sex in column and suicide/100k pop to columns and year at filter.

![Sheet 3](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/d484e1f8-7705-436f-9253-7bfe1b9e0941)
 
Result: From this we can tell that male is commiting more suicides.

The below bar plot has age in rows and sucide/100k pop in columns and color as gender. We can filter based on which contry we want.

![Sheet 4](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/d7c4530d-1aa3-4307-aa46-948047546a1b)
 
Result: From this we can tell that male who are 75 years and above have high suicide rates. Again, we check this for each country.
How has this changed over a given period?
Line graph:
I have used a line plot for this. Drag year to columns and suicide/100k pop to rows. And filter and year as filter. Sex as color.


![Sheet 5](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/81973d5e-2834-4173-b32e-9e0dce73ec62)

 
Result: From this we can say that male has more suicide rate compared to female and the difference is huge high, also in the period of 1994 to 1996 there were more suicide rates compared to other years. 

5.	 Understanding the Impact of Generation on Suicide Rates
How do suicide rates differ across different generations?
Bubble chart
For this graph, for each bubble a generation we display suicide/100k pop and year and sex as population. The color would be generation and size would be suicide/100k pop.

![Sheet 6](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/d2be9b96-0d2a-4035-b77c-e9d6007718ed)

 
Result: Silent generation have more suicide rates and we check this for each year and for each gender because this may change accordingly.
Is there any generational pattern in suicide rates, and how has it changed over the years?
Line graph:
For this I have used a line graph. Year in column, suicide/100kpop and generation as color. Each line represents a generation.

![Sheet 7](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/e179e65c-7e5f-4ff6-b812-b32e2967a173)



Result: Mostly the Silent generation topped from 2000 to 2012 and before this G.I Generation has topped. From this graph we can say that there is no interesting pattern for suicide rates based on generation at the given time.

6.	Top 5 highest and lowest suicide rate country.
Bar plot:
For this, I have used barplot. Suicide/100k pop in column, country in rows and year as filter. To get top 5, click on suicide/100k pop dropdown and select quick table calculation and select rank. Next click on country dropdown and select filter and select top and then select by field, top 5 click ok.

![Sheet 8](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/af6296b4-7ed8-4fae-a5ba-746123975e0a)
 
Result: Top 5 countries with highest suicide rates have been represented in above bar plot, they are Russian Federation, Lithuania, Hungary, Kazakhstan, Republic of Korea.
For Bottom 5:
Click on suicide/100k pop dropdown and select quick table calculation and select rank. Next click on country dropdown and select filter and select top and then select by field, bottom 5 click ok.

![Sheet 9](https://github.com/SreeKurapati6/Visualizing-Suicide-Trends-Exploring-Patterns-and-Influencing-Factors/assets/52539814/a92bdad0-2b84-448a-89ae-141f655ce755)
 
Result: Top 5 countries with lowest suicide rates have been represented in above bar plot, they are Dominica, Saint Kitts and Nevis, Oman, United Arab Emirates, Jamaica.

Discussion:
Most of the suicides are committed by Silent Generation.
Russia is the country with the highest rates number of suicide rates.
Based on these statistics, more men than women commit suicide.
In this data on suicides, older age groups make up a larger portion.
Also, there is a negative relation between GDP and suicide rate.
Conclusion:
This project is used to analyze suicide data, letting us know about the gender, generation which is committing suicide more. Also, we have examined the relation between GDP and suicide rate.
Reference:
https://en.wikipedia.org/wiki/Greatest_Generation#:~:text=The%20Greatest%20Generation%2C%20also%20known,born%20from%201901%20to%201927.
https://rixrewards.com/silents-boomers-gen-x-millennials-gen-z-and-alphas-who-how-why/
