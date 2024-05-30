# Mental Health Exploratory Data Analysis in Python

This **[Mental Health Dataset](https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset)** is a Real-World dataset that contains a variety of features related to text analysis, sentiment analysis, and psychological indicators, likely derived from posts or text data. These are the columns `Timestamp`, `Gender`,`Country`, `Occupation`, `self_employed`, `family_history`, `treatment`,`Days_Indoors`, `Growing_Stress`, `Changes_Habits`, `Mental_Health_History`, `Mood_Swings`, `Coping_Struggles`, `Work_Interest`, `Social_Weakness`, `mental_health_interview`, `care_options`

Check out the full code in this **[Kaggle notebook](https://www.kaggle.com/code/wilfridawere/mental-health-eda)**

Numerous analyses can be done using this dataset. I will focus on the following:

1. Gender Distribution in Mental Health Data by Country
2. Gender Distribution and Growing Stress: A Look at Different Occupations
3. Relationship Between Mental Health History, Growing Stress and Treatment Seeking Among Students by Country
4. Treatment-Seeking Behaviour: A Comparative Analysis of Men and Women

# Data Cleaning

The dataset has has 292364 rows and 17 columns





# 1. Gender Distribution in Mental Health Data by Country




# Insights from Analysis 1

The number of Female participants is **much lower** than Males. I'll convert counts to **proportions** for better comparison.
The way the data was collected might have led to an underrepresentation of Females.

The distribution of participants across countries is uneven. The ***United States*** has the highest number of participants, followed by the United Kingdom and Canada. ***Poland and Belgium*** are the only countries with a higher number of Women.

# 2. Gender Distribution and Growing Stress: A Look at Different Occupations

I aim to identify potential trends or relationships between ***Gender***,***Occupation***, and the presence of ***Growing Stress***

# Proportion of Growing Stress within each Gender



# Occupation vs. Growing Stress


# Gender Differences in Growing Stress Across Occupations



# Proportions of Growing Stress by Occupation & Gender


See the Heatmap below



# Insights from Analysis 2 

* A **higher proportion of Women** in all occupations but Business have reported experiencing Growing Stress. This is interesting considering there were fewer female participants.
* Regardless of Gender, specific occupations like **Corporate**, **Students** and **Housewife** report individuals with **high** Growing Stress respectively.

Feel free to conduct further analyses to investigate other factors that have relationships with Growing Stress.

# 3. Relationship Between Mental Health History, Growing Stress and Treatment Seeking Among Students by Country

# Co-occurrence of Mental Health History and Growing Stress in Students


# Distribution of Student Mental Health History by Country


# Treatment-Seeking Behaviour Among Students by Country and Mental Health History


# Treatment-Seeking Behaviour Among Students by Country and Growing Stress


# Insights from Analysis 3

First of all, it's important to remember that ***correlation doesn't necessarily imply causation***. In this case, I want to know if there's a relationship between Growing Stress and Mental Health History in Students. While stress might contribute to mental health issues, it's also possible that pre-existing mental health conditions can lead to increased stress. Other factors besides stress, such as academic pressure, social environment, or access to resources, could also be influencing mental health.

A significant number of students across all countries reported having some form of mental health history ("Maybe", "Yes"). This suggests a widespread need for mental health resources and support for students.

Those in ***Developed countries*** like United States, United Kingdom, Canada, Australia etc, have more students seeking Treatment. This is whether or not they reported having mental health history or Growing stress.

**Gap Between Need and Action**: While a number of students report mental health concerns,there seems to be a gap between those who need and those who seek treatment ("Yes"). This could indicate stigma around seeking help or lack of accessible resources.

# 4. Treatment-Seeking Behaviour: A Comparative Analysis of Men and Women




There are many other analyses you can perform using this Mental Health Dataset

Feel free to Contact me for any changes and feedback

***Explore and be teachable***
