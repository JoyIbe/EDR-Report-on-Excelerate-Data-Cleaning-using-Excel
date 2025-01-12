# EDR Report on Excelerate  Data Cleaning using Excel

## Introduction

In the context of analytical decision making, the ability to derive insights from data depends on a rigorous analysis and appreciation of datasets. The main objective of this Exploratory Data Analysis (EDA) report is to shed light on certain features, reveal patterns, and respond to complexities.
This groundwork is also preparatory to subsequent data processing and visualization but is also essential for the process of decision making. The significance of this EDA report is based on its ability to support Excelerate in its mission to improve user understanding and user experience, which in turn leads to the development of complex analytical dashboards.

#### Dataset Overview (User Data)

The focus of this analysis is on the “User Data” table, which has 8 columns and 27,563 rows. There are seven columns in the table, namely; “PreferredSponsors,” “Gender,” “Country,” “Degree,” “Sign Up Date,” “City,” “Zip” and “isFromSocialMedia.” This dataset includes basic background data of Excelerate users; therefore, it provides basic information on the nature of users. Every row corresponds to a distinct user and helps to assemble complete information. The specifics listed include user needs, age, location, date signed up, and social media logs, which serve as significant data that help in establishing and improving the user interaction on the platform.

#### Dataset Overview (Opportunity Sign Up Data)

The current analysis focuses on the “Opportunity Sign Up Data” which contains 21 columns and 20,322 records, and provides valuable information regarding the users’ engagement within the Excelerate application. The dataset offers great insights into user engagement, using categorical variables such as “Profile ID”, “Opportunity ID”, and numerical variables such as “Reward Amount”. Therefore, this EDA report strengthens the data quality aspect by using descriptive statistics, data visualization, and data cleaning techniques.
This report plays a crucial milestone in identifying user behaviors, preferences, and the results to enhance the user experience to appropriate optimum levels for further analysis. The exploration focuses on the difficulties that were faced during the data processing component, which demonstrated a highly rigorous process for validation. These insights will be useful in making strategic decisions and will help Excelerate achieve its top-level objective of improving user insights. This EDA is particularly valuable to Excelerate since it reveals hidden stories within the dataset, providing the organization with tools for a data-driven approach. Besides helping readers understand the details involved in dataset analysis, this report is essential to Excelerate’s mission since it can inform future analyses and serve as a basis for creating new and informative analytical dashboards.

## Data Examination:

#### User Data Overview

The Excelerate registration dataset contains information about 27,563 users, which provides a rich picture of the audience. It has eight columns, out of which PreferredSponsors is included that shows the user preference for the opportunity recommendations and Gender consisting of the unspecified entries. At registration, the system saves user locations through fields such as Country, Degree, City, and Zip while the academic level is captured in the Degree field. signup_date records account creation and isFromSocialMedia indicates Google Login sign-ups. The dataset has 94 PreferredSponsors, 169 countries, and 4016 cities. Degrees are grouped into: Undergraduate, High School, Graduate Program, Not in Education, and null with corresponding values. Out of the above results we can see that manual login got 13742 users while Google login got 13811 users. The availability of such demographic data enhances the possibility of differentiated analyses of opportunities that may be available on Excelerate as well as helping to develop suitable engagement strategies. It goes further in providing information on user qualities for enhanced decision making. The depth of the dataset is beneficial in developing more accurate and effective approaches, taking into account different geographical and academic backgrounds, improving the strategies of the Excelerate platform.

#### Opportunity Sign Up Data Overview

The primary object of study is the “Opportunity Sign Up Data” data set, which provides an overview of user activity in the Excelerate environment. With 20,322 rows and 21 columns, each value represents a different interaction and consists of a combination of numerical, categorical, and datetime data for the analysis. The “Profile ID” acts as an important alphanumeric reference number allowing for tracking of learner activity across the various opportunities. Since users are capable of signing up for various opportunities, the dataset expects the term “Profile ID” to appear multiple times. Also, the ‘Opportunity ID,’ an alphanumeric number that is assigned to each opportunity, helps sort user interactions and is used as a point of reference in the backend operations, with 33 different opportunities recorded.
This dataset can be described as a vast and diverse terrain, where one can wander in search of patterns, solve data anomalies, and mine for gold. Moving forward, the focus will be on improving users’ experiences on the Excelerate platform using the aforementioned identifiers like “Profile ID” and “Opportunity ID” as key reference points to decode specific user interactions and differentiate between opportunities. In this analytical process, we aim to make a valuable addition to the overarching goal of enhancing user interactions on the Excelerate platform.

## Column Analysis

In this segment, each of the columns included in the Opportunity Sign Up Data is assessed systematically. The process includes operations such as data type inspection, searching for possible issues with missing values and outliers, and providing brief descriptions for categorical variables.

### Column Analysis (User Data)

#### Preferred Sponsors:

Data Type: Text 

Description: This column shows the variety of sponsors selected by learners at the time of registration in the Excelerate Platform. In this case, learners are free to choose their sponsors and this makes it possible for them to get the kind of opportunities they prefer. They are free to select one or several sponsors depending on their desire for a more targeted approach and more suitable offers.


#### Gender:

Data Type: Categorical 

Description: This column shows the gender which was entered by the users at the time of registration in case they chose to provide that. It is not a mandatory field where a user is forced to provide their gender; rather, it is an optional field whereby the user has the freedom to input the gender they want or leave the field blank.

#### Country:

Data Type: Text

Description: On this column, it indicates the country the learner has stated that they live in at the time of registration.

#### Degree:

Data Type: Categorical

Description: This column displays the field of study that was mentioned by the user at the registration stage. This is something that users do not need to provide in order to sign up for the site.


#### Sign Up Date:

Data Type: Date

Description: This column indicates the date they signed up for an Excelerate account with the company.

#### City:

Data Type: Text

Description: This column shows the city that has been offered by the learner during the sign-up process for an experiment. It is an option, not an obligation that can be enforced or punished.

#### Zip:

Data Type: Text

Description:This column indicates the zip code of the city that the learner has provided upon registration as the area they reside in. This is not one of the entries that the users have to complete when they are creating their accounts.

#### isFromSocialMedia: 

Data Type: Boolean

Description: This column shows how the learners are registered, whether as individuals, in groups, or through an organization. A True value implies sign up through Google Login while a False value means signing up through the normal process without using Google Login details.

#### Cleaning Steps (User Data):

- Replaced "missing values", "blanks", "Don't Want to Specify", and "null"  with "Didn't Specify".
-  Converted date column from text to date format.
-   Ensured consistency across columns.
- Handled duplicate data points across categorical columns. 

### Data Types and Potential Issues (Opportunity Sign Up Data) 

#### - Profile ID (Alphanumeric):

Data Type: Alphanumeric Unique Identifier: Yes

No missing values identified.

#### Opportunity ID (Alphanumeric):

Data Type: Alphanumeric Unique Identifier: Yes

No missing values identified.

#### Opportunity Name (Categorical):

Data Type: Categorical

No missing values identified.

Unique Values: 33 opportunities with varying frequencies.

#### Opportunity Category (Categorical):

Data Type: Categorical

No missing values identified.

Unique Values: Event, Course, Competition, Internship, Engagement.

#### Opportunity End Date (Datetime):

Data Type: Datetime

No missing values identified.

Dates appear to follow a standardized format.

#### Gender (Categorical):

Data Type: Categorical

One missing value identified.

Unique Values: Male, Female, Don't want to specify, Other.


#### Cleaning Steps  (Opportunity Sign Up Data):

- Numerical columns like “Reward Amount” and Skilled Points Earned” were moderately skewed positively and negatively respectively. Hence, replacing the missing values with the median.

-  Using Text-to-Column dates were converted from text to date format.

- Replaced "missing values", "blanks", "Don't Want to Specify", and "null"  with "Didn't Specify".

- Ensured consistency across columns.

- Handled duplicate data points across categorical columns. 

#### Categorical Column Summaries

#### Gender:

Male: 60.23% (12,240)

Female: 39.39% (8,004)

Other categories: Don't want to specify, Other.

#### Current Student Status:

Graduate Program Student: 9,297 (45.75%)

High School Student, Undergraduate Student, Not in Education.

#### Opportunity Category:

Internship: 75.58%

Course:  8.51%

Event: 9.88% Other Categories.

#### Opportunity Name:

Data Visualization:27.98%

Project Management: 19.23%.

Digital Marketing: 12.20%

Other include percentages below 10%

#### Status Description:

Team Allocated: 69.90%

Dropped Out, Rejected, Applied, and others.

#### Applied Date Sign Ups:

June, 2023: 23.73%

The months of June, July and August are the top 3 months with the highest Applied Date Signups, ranging between 4823 and 3502. December, 2022 has the least Applied Date Sign Ups of 131.

#### Badge Name:

Unknown: 91.23%

Data Visualization Internship Completed: 1.93% Data Visualization Internship Star Performer: 1.33%

Project Management: 1.07%

The other categories take up the remaining percentage.

#### Key Observations:
Gender distribution is predominantly male.

"Graduate Program Student" is the most common status, followed by other student categories. "Internship" is the most frequent opportunity category.

The prevailing category for Badge Name is "Didn’t Specify," which indicates a large number of active learners still enrolled in the program. The distribution of Applied Date Sign Ups shows the counts are higher in some months than others, especially June, July and August. 

This analysis provides a comprehensive overview of Opportunity Sign Up Data with focus on specific features, possible weaknesses, and distribution of columns by categories. The obtained information creates a basis for the further stages of data analysis and visualization to make more accurate conclusions and further investigation.


#### Profile ID Analysis

In this section, we delve into the analysis of the "Profile ID" column, examining the uniqueness of Profile IDs, and identifying instances of duplicates or missing values.

#### Uniqueness of Profile IDs (Opportunity Sign Up Data)

1. The dataset contains a total of 11,481 unique Profile IDs.

2. Duplicate Profile IDs (Opportunity Sign Up Data)
   
Instances of duplicate Profile IDs were identified:

"c2245f7e-2e9d-42c9-b5af-550be9eae1c8" and "18e1e6bc-fada-4b09-bf52-ab45daf318f4" are tied for the highest count at 22.
Followed by other counts of 21, 20, etc.

4. Missing Profile IDs (Opportunity Sign Up Data)

No instances of missing Profile IDs were identified.

#### Key Observations:
This dataset presents a great number of different Profile IDs, which indicates the range of users’ activity. As a matter of fact, it is worthy to note that some of the Profile IDs appear more than once meaning that the users have been interacting with the platform in different instances. The detailed examination of the most significant ‘Profile ID’ reveals the range of diversity of users’ activity. The presence of duplicate IDs suggests that some individuals engaged in several events within the Excelerate context. It is also crucial in understanding users’ actions to plan further interaction on this website. In addition, the fact that there are no missing Profile IDs makes the data more reliable and comprehensive in this crucial identifier.

#### Opportunity Status Distribution

Here we concentrate on the "Status Description" column in the Opportunity Sign Up Data, providing a distribution summary of the different statuses and their occurrences.

Status Description | Count of Status Description
|---|---|
Applied | 89
Dropped Out | 24
Not Started | 1,324
Rejected| 726
Rewards Award | 2,521
Started| 810
Team Allocated | 14,206
Withdraw | 622


#### Key Observations:

The prevalence of "Team Allocated" in the Status Description column signifies a considerable number of participants successfully assigned to teams. 

Similarly, the substantial count of "Rewards Award" indicates recognition for a noteworthy portion of participants. Noteworthy counts for "Not Started" and "Rejected" reflect participants at different stages of engagement. 

Analyzing this status distribution is pivotal for assessing the success and impact of opportunities on the Excelerate platform.

The dominance of positive statuses like "Team Allocated" and "Rewards Award" suggests a significant level of achievement and acknowledgment. Evaluating the varied statuses provides valuable insights into the progression and outcomes for participants across diverse opportunities.

### Basic Statistics

The User Data dataset is not very suitable for statistical analysis, as there are no numeric columns, which prevents the provision of quantitative conclusions. The lack of numerical values limits the investigation of the relations and trends in the user data. However, the subsequent section covers the Opportunity Sign Up Data where fundamental statistics such as mean, median, min, and max are calculated for the relevant numeric fields to allow for statistical analysis.

#### Reward Amount (Opportunity Sign Up Data):

Mean: 1081.261

Median: 500

Minimum: 50

Maximum: 2500

Standard Deviation: 927.251

Range: 2450

Sum: 2,725,860

Count: 2521

Skewness: 0.7

#### Skill Points Earned (Opportunity Sign Up Data):

Mean: 1186.965

Median: 1182

Minimum: 10

Maximum: 1776

Standard Deviation: 4399.172

Range: 1776

Sum: 2,992,338

Count: 2521

#### Key Observations:
The “Reward Amount” in the dataset has a wide spread with a right-skewed distribution and notable variability. While “Skilled Points Earned” is fairly symmetrically distributed with a slight left skew and moderate variability. Calculating basic statistics offers a quantitative grasp of the distribution and variability, providing valuable insights into the impact of opportunities on the Excelerate platform and revealing patterns in participant performance. It also provides a blueprint for handling its missing values, prioritizing well-considered and strategic decision-making.

## Initial Observation

#### User Data

Structure of Data: Dataset consists of 8 columns and 27.563 rows.

Date Column: The date column required cleaning-up because of its inability to perform arithmetic operations with its text datatype.

Diversity in Data: In the given data set case, there are some countries for which there are one  and fewer samples and there are some countries for which there are more than a thousand samples.

#### Key Insights:

Social media marketing:

- Social media marketing started in Mar.2023 and the total registered user between Mar - Dec 2023 was (13,811), while the total number of registrations without social media marketing was (9,369) in the same period. There was a 47% increase in registration through social media marketing compared with the regular registration.
  
- 32 new countries were added to the list of coverage areas after the implementation of social media marketing.
  
- The highest number of registrations happened in June for 2022 & 2023, followed by July.


#### Recommendation:

- Increase more engagement on social media to add more users to the platform and also to reach more countries

- More support staff should be available to handle more requests during the peak of registration in June as seen on the visualization "Registered User by Social Media Marketing".

#### Opportunity Sign Up Data

During the exploratory analysis of the Opportunity Sign Up Data, several initial observations and patterns emerged:

#### Status Distribution

The largest portion of the participants is in the “Team Allocated” state, which shows high rates of successful teaming.

There were a significant number of participants who did not get rewarded as the “Rewards Award” status depicted very low completion on the program.

The percentage of participants that have not even begun or have been turned down is quite high.

#### Profile IDs

There are Profile IDs of various users, which may or may not have a high level of interaction with the Excelerate platform. There are Profile IDs that are repeated, which implies that there are some people who have signed up for more than one opportunity.

#### Reward and Skill Points

The "Reward Amount" and "Skill Points Earned" columns exhibit wide ranges, with some participants receiving high rewards or earning a significant number of skill points. Negative values in the "Reward Amount" column suggest cases where participants were Withdrawn, Dropped Out, and Rejected.

#### Badge Information

The "Badge ID" column includes repetitions, indicating instances where multiple participants earned the same type of badge.


#### Missing Values

There were instances where certain columns in the dataset contained missing values, and depending on the type of information and the status of the participants’ description, different approaches were taken.


## Areas of Interest for Deeper Investigation:

#### Status Progression Analysis: 

- Examine how the participants demographically move from one status level to the other. Explore reasons for non initiation and refusal by the participants.

#### User Engagement Patterns:

- It remains possible to consider the frequency of engagements for users with multiple instances of the Profile IDs. 

- Examine potential users who have signed up for various opportunities.

#### Impact of Rewards and Skill Points:

- We also could investigate how rewards and skill points may influence the participants’ activity and results. 

- Research on instances where people did not get incentives despite participation.

#### Badge Achievements:

- Examine the importance and effectiveness of particular badges.

-Examine how the badge achievements are distributed and if there are any relationships with other participant characteristics.

#### Data Quality and Missing Values:

Make sure to perform a detailed inspection of cases with missing data and their effect on the analysis. Reflect on possible causes of missing values in particular columns and evaluate their significance.

These initial observations provide an outline for further examination in the next weeks, as the main goal is to collect more data regarding the participation rates, success levels, and the efficiency of opportunities within the Excelerate platform.


## Visualizations

### User Data Viz:

![User_Gender](https://github.com/user-attachments/assets/07213009-48e1-4000-96be-ec84b06e25ab)

![User_Degree](https://github.com/user-attachments/assets/307e6c3c-2832-4bd0-98d1-27605d2a8c28)

![User_Yearly Signup](https://github.com/user-attachments/assets/0c3f1e34-8a92-428d-b14a-f958794377ee)

![User_Social](https://github.com/user-attachments/assets/ba9969af-5fe8-44a7-baf2-d2dad2db5d67)

![User_GenderDegree](https://github.com/user-attachments/assets/2cc1f29f-72fe-43aa-a7f2-2993dad91e0b)

### Opportunity Sign Up Data Viz:

![Opp_Gender](https://github.com/user-attachments/assets/7f58a9e2-186c-4f36-9817-32967bbc3775)

![Opp_CurrentStat2](https://github.com/user-attachments/assets/dfc6a01b-1d30-4571-bb9d-a6653310cfc4)

![Opp_Cat](https://github.com/user-attachments/assets/e1241bbf-c044-4ed1-a379-2debcf75c9bb)


![Opp_AppliedDate](https://github.com/user-attachments/assets/037150c2-92d3-4bcb-822e-f85ebc297f53)

![Opp_BadgeName](https://github.com/user-attachments/assets/8bbe672d-94e5-47d9-8b5d-1e48f5dc7b8d)


![Opp_Reward](https://github.com/user-attachments/assets/6c8b7884-ce1e-4066-971f-0253634062d2)

## Challenges Faced

### Data Validation:

There are countries in the dataset represented by one or two individuals, which are considered outliers indicative of inaccurate data.

### Incomplete and Unclear Dataset:

A minimum of five out of eight columns contain null, blank, or missing values, impacting the precision of the data analysis.

### Continuous Data Monitoring:

Data quality over time can become an issue due to several factors; which may include the updated source of the data, the data collection method, and users’ behaviors. Hence, the use of plans for monitoring and managing data in the long-term is important in the pursuit of sustaining the validity and coherence of the dataset for future use.

## Next Steps

The process of creating a comprehensive dashboard for Excelerate leadership requires a strategic approach to answering critical questions. The purpose is to create an interface with information on platform usage, geographical presence, interaction, opportunity preference, completion rates, demographics, skill enhancement, and scholarships awarded. In the following weeks, a careful investigation of feature analysis and data processing shall take place, from which deeper insights will be extracted and woven into subsequent reports.

## Conclusion

In terms of the participants’ demographics and their sign up behaviors, the dataset offers crucial information.
The nature of the sponsors and educational background of the participants can be used to guide the development of the marketing campaigns or the educational materials.
The inclusion of other numerical data like the sign up date or any other relevant data could offer deeper information on the trends and cycle patterns.








