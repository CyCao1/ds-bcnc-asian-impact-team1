# For different .ipynb files we uploaded:

1. occupation: Showing basic info about our dataset; Showing mean salary with different asian subgroups in 2015-2019; Dealing with occupation distribution within the Asian sub-groups. Top 10 occupations are listed. Also one generalized occupation distribution is grabbed.(In orginal dataset there are over 300 occupations; after generalization, there are groupped into 16)


2. features_mean_salary: Dealing with relationship of mean salary with age/sex/education

# To navigate our dataset:

1. Our final dataset(usa_preprocessed.csv) is retrieved from IPUMS and merged by 2015-2019 samples in the USA(ipums_usa.csv) and the CPS(ipums_cps.csv) sites. (The jupyter notebook used to merge two datasets is included in the repo Team1 branch.)

2. IPUMS fills the column values with specific codes to indicate true meaning, and we have translated part of the codes into human readable text. To get what those original codes indicate, please visit [ ACS search ](https://usa.ipums.org/usa-action/variables/search) and [ CPS search ](https://cps.ipums.org/cps-action/variables/search), and search for the column names.

3. Meaning of features in our merged dataset is listed below:


    |  FEATURE   | Meaning  |
    |  :----:  | :----  |
    | [ YEAR ](https://cps.ipums.org/cps-action/variables/search)  | Census year |
    | [ STATEFIP ](https://usa.ipums.org/usa-action/variables/STATEFIP)  | State (FIPS code) |
    | [ CITY ](https://usa.ipums.org/usa-action/variables/CITY)  | City |
    | [ SEX ](https://usa.ipums.org/usa-action/variables/SEX)  | Sex |
    | [ AGE ](https://usa.ipums.org/usa-action/variables/AGE)  | Age |
    | [ RACED (detailed) ](https://usa.ipums.org/usa-action/variables/RACE)  | Race [detailed version] (Asian subgroups) |
    | [ EDUC (general) ](https://usa.ipums.org/usa-action/variables/EDUC)  | Educational attainment [general version] |
    | [ EMPSTAT (general) ](https://usa.ipums.org/usa-action/variables/EMPSTAT)  | Employment status [general version] |
    | [ OCC2010 ](https://usa.ipums.org/usa-action/variables/OCC2010)  | Occupation, 2010 basis |
    | [ IND ](https://usa.ipums.org/usa-action/variables/IND)  | Industry |
    | [ UHRSWORK ](https://usa.ipums.org/usa-action/variables/UHRSWORK)  | Usual hours worked per week |
    | [ INCTOT ](https://usa.ipums.org/usa-action/variables/INCTOT)  | Total personal income |
    | [ INCWAGE ](https://usa.ipums.org/usa-action/variables/INCWAGE)  | Wage and salary income |
    
    [Note: To extract a dataset with desired variables(features), please visit [ IPUMS USA ](https://usa.ipums.org/usa/) or [ IPUMS CPS ](https://cps.ipums.org/cps/) and click “**Get Data**”, then navigate the lists under “**SELECT HARMONIZED VARIABLES**”.]


# To reproduce our results:

1. Please first extract data from IPUMS using the same variables shown in the report and change the data format into csv in the “**Extract Request**” page. Then click “**Select cases**” in the Options and only select cases such that STATEFIP=25, RACED is Asians, and RACASIAN =2. Save the extracted files as “ipums_usa.csv” and “ipums_cps.csv”.

2. Put the downloaded files in the same directory as the jupyter notebooks. First of all, if ACS and CPS datasets are downloaded, run “merge_dataset.ipynb” to merge the two. Secondly, run “occupation.ipynb” to get the preliminary analysis, average salary of the data, and occupational choices. Lastly, “features_mean_salary.ipynb” produces graphs that illustrate relationships of mean salary with age/sex/education.



# Add Users
To add yourself to the repository, open a Pull Request modifying `COLLABORATORS`, entering your GitHub username in a newline.

All Pull Requests must follow the Pull Request Template, with a title formatted like such `[Project Name]: <Descriptive Title>`



