# Mental Health Exploratory Data Analysis in Python

This **[Mental Health Dataset](https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset)** is a Real-World dataset that contains a variety of features related to text analysis, sentiment analysis, and psychological indicators, likely derived from posts or text data. These are the columns `Timestamp`, `Gender`,`Country`, `Occupation`, `self_employed`, `family_history`, `treatment`,`Days_Indoors`, `Growing_Stress`, `Changes_Habits`, `Mental_Health_History`, `Mood_Swings`, `Coping_Struggles`, `Work_Interest`, `Social_Weakness`, `mental_health_interview`, `care_options`

Check out the full code in this **[Kaggle notebook](https://www.kaggle.com/code/wilfridawere/mental-health-eda)**

Numerous analyses can be done using this dataset. I will focus on the following:

1. Gender Distribution in Mental Health Data by Country
2. Gender Distribution and Growing Stress: A Look at Different Occupations
3. Relationship Between Mental Health History, Growing Stress and Treatment Seeking Among Students by Country
4. Treatment-Seeking Behaviour: A Comparative Analysis of Men and Women

# Data Cleaning

The dataset has has 292,364 rows and 17 columns

There are 1.8% missing values in the `self_employed` column so dropping those rows will not affect the data significantly.

The Percentage of Duplicated rows in the dataset is 0.8%. Dropping them works too.

# 1. Gender Distribution in Mental Health Data by Country

**Distribution of Gender in Mental Health Data**

![Alt text](./Distribution%20of%20Gender%20in%20Mental%20Health%20Data.png)

**Distribution of Countries in Mental Health Data**

![Alt text](./Distribution%20of%20Countries%20in%20Mental%20Health%20Data.png)

**Distribution of Countries in Mental Health Data by Gender**

| Gender | Female | Male | Total |
|---|---|---|---|
| United States | 34049 | 131820 | 165869 |
| United Kingdom | 6896 | 43680 | 50576 |
| Canada | 3879 | 13650 | 17529 |
| Australia | 1724 | 4290 | 6014 |
| Netherlands | 431 | 5460 | 5891 |
| Ireland | 862 | 4680 | 5542 |
| Germany | 0 | 4680 | 4680 |
| Sweden | 862 | 1950 | 2812 |
| India | 431 | 2340 | 2771 |
| Brazil | 0 | 2340 | 2340 |
| France | 0 | 2340 | 2340 |
| South Africa | 431 | 1560 | 1991 |
| New Zealand | 431 | 1560 | 1991 |
| Switzerland | 0 | 1560 | 1560 |
| Italy | 0 | 1560 | 1560 |
| Israel | 0 | 1560 | 1560 |
| Poland | 431 | 390 | 821 |
| Belgium | 431 | 390 | 821 |
| Denmark | 0 | 780 | 780 |
| Singapore | 0 | 780 | 780 |
| Russia | 0 | 780 | 780 |
| Greece | 0 | 780 | 780 |
| Finland | 0 | 390 | 390 |
| Nigeria | 0 | 390 | 390 |
| Philippines | 0 | 390 | 390 |
| Moldova | 0 | 390 | 390 |
| Portugal | 0 | 390 | 390 |
| Colombia | 0 | 390 | 390 |
| Georgia | 0 | 390 | 390 |
| Czech Republic | 0 | 390 | 390 |
| Croatia | 0 | 390 | 390 |
| Costa Rica | 0 | 390 | 390 |
| Thailand | 0 | 390 | 390 |
| Bosnia and Herzegovina | 0 | 390 | 390 |
| Mexico | 0 | 390 | 390 |

# Insights from Analysis 1

The number of Female participants is **much lower** than Males. I'll convert counts to **proportions** for better comparison.
The way the data was collected might have led to an underrepresentation of Females.

The distribution of participants across countries is uneven. The ***United States*** has the highest number of participants, followed by the United Kingdom and Canada. ***Poland and Belgium*** are the only countries with a higher number of Women.

# 2. Gender Distribution and Growing Stress: A Look at Different Occupations

I aim to identify potential trends or relationships between ***Gender***,***Occupation***, and the presence of ***Growing Stress***

## Proportion of Growing Stress within each Gender

| Gender | Count |
|---|---|
| Male | 234000 |
| Female | 50858 |

| Growing_Stress | Female | Male |
|---|---|---|
| Maybe | 0.301624 | 0.351282 |
| No | 0.301624 | 0.320513 |
| Yes | 0.396752 | 0.328205 |

## Occupation vs. Growing Stress

| Growing_Stress | Business | Corporate | Housewife | Others | Student |
|---|---|---|---|---|---|
| Maybe | 16632 | 16632 | 23576 | 17950 | 22750 |
| No | 13868 | 19642 | 22032 | 18550 | 16248 |
| Yes | 18422 | 23340 | 19120 | 14930 | 21166 |

## Gender Differences in Growing Stress Across Occupations

The responses to `Growing_Stress` were Maybe, No and Yes

| Occupation | Gender | Maybe | No | Yes |
|---|---|---|---|---|
| Business | Female | 2832 | 3068 | 3422 |
| | Male | 13800 | 10800 | 15000 |
| Corporate | Female | 2832 | 2242 | 3540 |
| | Male | 13800 | 17400 | 19800 |
| Housewife | Female | 3776 | 2832 | 4720 |
| | Male | 19800 | 19200 | 14400 |
| Others | Female | 2950 | 2950 | 4130 |
| | Male | 15000 | 15600 | 10800 |
| Student | Female | 2950 | 4248 | 4366 |
| | Male | 19800 | 12000 | 16800 |

## Proportions of Growing Stress by Occupation & Gender

| Occupation | Gender | Maybe | No | Yes |
|---|---|---|---|---|
| Business | Female | 0.303797 | 0.329114 | 0.367089 |
| | Male | 0.348485 | 0.272727 | 0.378788 |
| Corporate | Female | 0.328767 | 0.260274 | 0.410959 |
| | Male | 0.270588 | 0.341176 | 0.388235 |
| Housewife | Female | 0.333333 | 0.250000 | 0.416667 |
| | Male | 0.370787 | 0.359551 | 0.269663 |
| Others | Female | 0.294118 | 0.294118 | 0.411765 |
| | Male | 0.362319 | 0.376812 | 0.260870 |
| Student | Female | 0.255102 | 0.367347 | 0.377551 |
| | Male | 0.407407 | 0.246914 | 0.345679 |

See the Heatmap below

![Alt text](./Proportion%20of%20Growing%20Stress%20by%20Occupation%20and%20Gender.png)

# Insights from Analysis 2 

* A **higher proportion of Women** in all occupations but Business have reported experiencing Growing Stress. This is interesting considering there were fewer female participants.
* Regardless of Gender, specific occupations like **Corporate**, **Students** and **Housewife** report individuals with **high** Growing Stress respectively.

Feel free to conduct further analyses to investigate other factors that have relationships with Growing Stress.

# 3. Relationship Between Mental Health History, Growing Stress and Treatment Seeking Among Students by Country

## Co-occurrence of Mental Health History and Growing Stress in Students

![Alt text](./Co-occurrence%20of%20Mental%20Health%20History%20and%20Growing%20Stress%20in%20Students.png)

## Distribution of Student Mental Health History by Country

`Mental_Health_History` has 3 options; Maybe, No, and Yes. We take a look at how Students in different countries responded.

| Mental_Health_History | Maybe | No | Yes | Total |
|---|---|---|---|---|
| United States | 11790 | 13085 | 10245 | 35120 |
| United Kingdom | 3520 | 4000 | 3120 | 10640 |
| Canada | 1252 | 1382 | 1083 | 3717 |
| Australia | 438 | 473 | 372 | 1283 |
| Netherlands | 402 | 467 | 363 | 1232 |
| Ireland | 388 | 438 | 342 | 1168 |
| Germany | 312 | 372 | 288 | 972 |
| Sweden | 206 | 221 | 174 | 601 |
| India | 194 | 219 | 171 | 584 |
| Brazil | 156 | 186 | 144 | 486 |
| France | 156 | 186 | 144 | 486 |
| South Africa | 142 | 157 | 123 | 422 |
| New Zealand | 142 | 157 | 123 | 422 |
| Switzerland | 104 | 124 | 96 | 324 |
| Italy | 104 | 124 | 96 | 324 |
| Israel | 104 | 124 | 96 | 324 |
| Poland | 64 | 64 | 51 | 179 |
| Belgium | 64 | 64 | 51 | 179 |
| Denmark | 52 | 62 | 48 | 162 |
| Singapore | 52 | 62 | 48 | 162 |
| Russia | 52 | 62 | 48 | 162 |
| Greece | 52 | 62 | 48 | 162 |
| Finland | 26 | 31 | 24 | 81 |
| Nigeria | 26 | 31 | 24 | 81 |
| Philippines | 26 | 31 | 24 | 81 |
| Moldova | 26 | 31 | 24 | 81 |
| Portugal | 26 | 31 | 24 | 81 |
| Colombia | 26 | 31 | 24 | 81 |
| Georgia | 26 | 31 | 24 | 81 |
| Czech Republic | 26 | 31 | 24 | 81 |
| Croatia | 26 | 31 | 24 | 81 |
| Costa Rica | 26 | 31 | 24 | 81 |
| Thailand | 26 | 31 | 24 | 81 |
| Bosnia and Herzegovina | 26 | 31 | 24 | 81 |
| Mexico | 26 | 31 | 24 | 81 |

## Treatment-Seeking Behaviour Among Students by Country and Mental Health History

For the following Tables, see the full outputs **[Here](https://www.kaggle.com/code/wilfridawere/mental-health-eda)**

![Alt Text](./Treatment-Seeking%20Behaviour%20Among%20Students%20by%20Country%20and%20Mental%20Health%20History%20table1.jpg)

![Alt Text](./Treatment-Seeking%20Behaviour%20Among%20Students%20by%20Country%20and%20Mental%20Health%20History%20tablepart2.jpg)

## Treatment-Seeking Behaviour Among Students by Country and Growing Stress

![Alt Text](./Treatment-Seeking%20Behaviour%20Among%20Students%20by%20Country%20and%20Growing%20Stress.jpg)

# Insights from Analysis 3

First of all, it's important to remember that ***correlation doesn't necessarily imply causation***. In this case, I want to know if there's a relationship between Growing Stress and Mental Health History in Students. While stress might contribute to mental health issues, it's also possible that pre-existing mental health conditions can lead to increased stress. Other factors besides stress, such as academic pressure, social environment, or access to resources, could also be influencing mental health.

A significant number of students across all countries reported having some form of mental health history ("Maybe", "Yes"). This suggests a widespread need for mental health resources and support for students.

Those in ***Developed countries*** like United States, United Kingdom, Canada, Australia etc, have more students seeking Treatment. This is whether or not they reported having mental health history or Growing stress.

**Gap Between Need and Action**: While a number of students report mental health concerns,there seems to be a gap between those who need and those who seek treatment ("Yes"). This could indicate stigma around seeking help or lack of accessible resources.

# 4. Treatment-Seeking Behaviour: A Comparative Analysis of Men and Women

**Proportion of Individuals Seeking Treatment by Gender**

![Alt text](./Proportion%20of%20Individuals%20Seeking%20Treatment%20by%20Gender.png)

There are many other analyses you can perform using this Mental Health Dataset

Feel free to Contact me for any changes and feedback

***Explore and be teachable***
