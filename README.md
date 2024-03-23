# Indian Start Up Funding Ecosystem

# Project Description
My team is trying to venture into the Indian start-up ecosystem. This project aims to provide insights into the Indian startup ecosystem through data analysis. The analysis includes cleaning and processing raw data, exploring various aspects of the startup landscape, and deriving meaningful conclusions

### Team Lead
Ntuk, Etebom

## Collaborators
Mohammed Idris
Etebom Ntuk
Elvis Obeng Yeboah
Prince Acquah Rockson
Celestine Jerop Kaplelach
Andy Konney

### Table of Contents

## Introduction

## Business Understanding

## Data Understanding and Preparation

## Data Analysis Methods

## Data Representation

## Final Findings

## Usage

## Contributions

## License

## Introduction

India has emerged as one of the most vibrant startup ecosystems globally. This project delves into understanding the dynamics of this ecosystem by analyzing relevant data. By examining factors such as funding trends, sectoral distribution, geographical concentration, and success metrics, we aim to uncover patterns and insights crucial for stakeholders in the startup space.

# Business Understanding
The primary objective of our project is to venture into the Indian Start Up Ecosystem. This involves understanding the landscape of the start ups in India, their funding patterns, and the key players in the system i.e Investors and Startups.

## Data Understanding and Preparation
## Data Cleaning and Data Exploration

The data used in this analysis was sourced from three different sources, github, sql server and onedrive, a connection was created with a connection string defined in the '.env' file

1. Data Collection: Gathering raw data from online database.
   # Access the 2018 dataset
url = 'https://raw.githubusercontent.com/Azubi-Africa/Career_Accelerator_LP1-Data_Analysis/main/startup_funding2018.csv'

dat1 = pd.read_csv(url)
dat1

# Access the 2019 dataset

dat2 = pd.read_csv('dataset/startup_funding2019.csv')
dat2

# select data from 2020
query = "SELECT * FROM LP1_startup_funding2020"

dat3 = pd.read_sql(query, connection)
dat3.head()

# loading data from 2021
query = "SELECT * FROM LP1_startup_funding2021"

dat4 = pd.read_sql(query, connection)
dat4.head()

2. Data Integration: Consolidating data from different sources into a unified dataset.

#merging 2020 and 2021 datasets
merged_table= pd.concat([dat3, dat4], ignore_index=True)
merged_table

#merging 2019,2020,2021
merger= pd.concat([dat2, merged_table], ignore_index=True)
merger

#merging 2018,2019,2020,2021
data_df= pd.concat([dat1, merger], ignore_index=True)
data_df

3. Missing Value Handling: Identifying and dealing with missing values through imputation or removal.

4. Outlier Detection: Detecting and handling outliers that could skew the analysis results.

5. Normalization and Standardization: Ensuring consistency and comparability of data by normalizing or standardizing where necessary.

5. Data Validation: Verifying the integrity of the cleaned dataset to ensure accuracy in subsequent analyses..

## Data Analysis Methods

Various analytical methods and techniques were utilized to extract insights from the data:

1. Descriptive Statistics: Summarizing key metrics such as mean, median, mode, and standard deviation to describe the central tendency and dispersion of variables.
2. Time-Series Analysis: Examining trends and patterns over time to understand the evolution of the startup ecosystem.
3. Correlation Analysis: Investigating relationships between different variables, such as funding amount and startup success rate.
4. Segmentation Analysis: Grouping startups based on common characteristics (e.g., sector, funding stage) and analyzing each segment separately.
5. Predictive Modeling: Building predictive models to forecast future trends or identify factors influencing startup performance.

## Data Visualization

The cleaned data was represented in structured formats suitable for analysis. This included;
1. Organizing data into tables and saving the unified dataset as a single '.csv' file.
2. Visualization techniques such as charts, graphs, and maps were also employed to present key findings effectively.

## Data Deployment
In our project we use Power BI dashboard to deploy our data

## Final Findings

Based on the analysis conducted, several key findings emerged:

1. Sectoral Trends: Identification of sectors experiencing rapid growth and emerging as key drivers of the Indian startup ecosystem.
2. Funding Patterns: Insights into the sources and distribution of funding across different stages of startup development.
3. Geographical Insights: Understanding regional variations in startup activity and investment flows within India.
4. Success Factors: Identification of factors correlated with startup success, including funding amount, team composition, and market positioning.
5. Challenges and Opportunities: Highlighting challenges faced by startups and opportunities for intervention and support from stakeholders.

## Usage

To replicate or extend the analysis conducted in this project, follow these steps:

1. Clone the Repository: Clone this repository to your local machine using git clone https://github.com/cjerop/analysis-into-indian-startup-ecosystem.git.

2. Install Dependencies: Ensure all necessary dependencies are installed as per the requirements specified in requirements.txt.
   pip install python-dotenv
   pip install pyodbc
   pip install numpy
   pip install pandas
   pip install seaborn
   pip install scipy
   pip install jupyterlab

## activate by using the script below

.\venv\Scripts\activate

3. Run Analysis Scripts: Execute the analysis scripts provided in the repository, following any instructions or guidelines provided in the README or code comments.

4. Explore Results: Explore the generated results, visualizations, and findings to gain insights into the Indian startup ecosystem.
   .\venv\Scripts\activate

## Contributions

Contributions to this project are welcome! If you have suggestions for improvement, new analyses to conduct, or additional data sources to incorporate, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License, which means you are free to use, modify, and distribute the code for any purpose, provided you include the appropriate license information. See the LICENSE file for more details.

## Conclusion

Based on our findings
The trend of amount received by founding year we realized funding started to increase for startups that were birthed from 2017 and it peaked in 2018. then dropped in 2019. it became static till then.

Finance industry dominated the others in terms of receiving funding. The next two were the technology companies and companies involved in business which had closely related Amount of funding.

Funding for Indian startups decreased between 2018 and 2019. and then it rose during 2020(COVID-19 era). Funding after this year rose incredibly
Mumbai had by far the greatest funding in terms of Amount received. the next four are Bangalore. New Delhi, Deli and Pune.

Bangalore was the home of most of the startups between this period. This was follwed by Mumbai, New Delhi, Gurugram and Delhi for the top 5
It was realised that Inflection point type of investors pumped in more money. Mumbai Angeln network and Angel Inbestors were next to them with almost same amount of money pushed into startups. Titan Capital and investors who were undiscloded were the next set of investors who pushed in more money,

Three major investors in the Indian start-up ecosystem and the industries they love to invest in ascending order the following industries : Techhnology(7), Business(5) and Education(5). Mumbai Angels Network invested most in Transport, Hospitality and Education (2 each). The third major investor, Ventue Catalysts invested in 6 each of Food & Beverages nad 5 for Technology
The highest rising industry was noted to be the Business industry where the rose from about 5 start ups in 2019. 125 new businesses joined them in 2020 and by 2021, they had about 115 new businesses. The next is eduaction which started at the same point as in the business industry but had just 80 new startups joining them in 20202 and 2021 each. the third is just engineering industry where they came to light in 2021 boasting of a about 10 start ups.

The first main sector gaining tractions from investors by counts is Technology. they had 70, 10, 140 and 120 companies. The second is AI, they had 10, 2, 40 and 8 from 2018 to 2021. finally the next main sector that was emerging as receiving funding was Fintech, 30, 2, 118 and 58 across the years.

Top 3 Main sectors in terms of funding received within the top 3 industries(Business,Technology, Transport). Business engulfed Business which was followed by E-commerce, Media & technology. For Technology, technology itself dominated the main sectors which was followed by Ai and then Ar/Vr. For the transport industry, the most dominating sectors were transport & logistics, automobile and aviation respectively. 

## Any Additional information
### Email Address
### Link to your Medium
## Author








