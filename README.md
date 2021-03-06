Voter Analytics for Bangalore
=============================

The aim of this project is to analyze pre and post-poll data of Bangalore, especially in regions where the voter turnout is lower than estimated. Although there can be several discrepancies which leads to low voter turn out such as mistakes in electoral rolls, mismatched voter IDs and missing name in polling days. This project aims to provide a voter analytics system for post-poll analysis.

Project Milestones and Progress
-------------------------------

| Milestones                                  | Status          |
| :-----------------------------------------: | :-------------: |
| Assembly Data Scraping                      | Complete        |
| Assembly Data Analysis                      | Complete        |
| Form 20 CSV Data Scraping                   | Complete        |
| Form 20 CSV Data Analysis                   | Complete        |
| Form 20 PDF Data Scraping                   | Complete        |
| Constituency wise Complete Data Gathering   | Complete        |
| Constituency wise Complete Data Scraping    | Complete        |
| Constituency wise Complete Data Analysis    | Complete        |
| Constituency wise Voter Data Scraping       | Complete        |
| Constituency wise Voter Data Analysis       | Complete        |
| Fuzzy Matching and Anomaly Detection        | Complete        |
| Choropleth Visualization                   | Complete        |
| Porting project to AWS                      | Complete        |
| Persisting data to backend MySQL db         | Complete        |
| Exposing data through RESTful API           | Complete        |
| Generating Insights from Form 20 data       | Complete        |

## Insights

These are some of the insights we gained from the 2014 Election Data for Hebbal Constituency -

1. Showcases number of votes gained by the candidates in the Hebbal constituency [http://i.imgur.com/L7OmAKE.png]

2. Number of votes each candidate got per booth in Hebbal Constituency (limited booth data shown for clarity) [http://i.imgur.com/xTvBAVo.png]

3. Heatmap for candidates showing votes received per booth (Green refers to large vote count, Red refers to low vote count) [http://i.imgur.com/3cFE5pd.png]

## Choropleth Visualization

We have drawn our visualization from the post electoral data and they are available below -

1. Statewise total number of voters for Karnataka - [http://bpacdata.appspot.com]

2. Statewise total number of 'male' voters for Karnataka - [http://bpacdata.appspot.com/male.html]

3. Statewise total number of 'female' voters for Karnataka - [http://bpacdata.appspot.com/female.html]

## Features


### Form 20 Data Analysis

Form 20 gives a deeper view to the electoral data. CEOs publish Form 20 after the election. In this project, we have worked on the 2014 Form 20 data for Hebbal constituency. The data was provided by BPAC.

### Constituency wise Data Analysis

Each constituency can be divided into different parts. Each part have their own polling booth where the number of actual voter turnout and number of registered voters available. For the Hebbal constituency, we have crawled 212 PDFs for each part and gathered registered voter data (male and female) for each part.

### Constituency wise Voter Data Analysis

Along with the registered voter data, each PDF also gives detailed information (Name, Husband/Mother/Fathers Name, Address, Gender and Age) for each voter. We have scraped each PDF file and gathered detailed information on each voter. This data will be used later for anomaly detection by fuzzy matching.

### Fuzzy Matching and Anomaly Detection

Used "fuzzywuzzy" library in Python for fuzzy string matching of voter data and detecting anomalies such as multiple entires in a booth, multiple entries across booths etc.

### Chloropleth Visualization

Choropleth map is a visulization that shows graded differences in shading inside defined areas on the map in order to indicate a quantity in those areas. We are aiming to show a constituency wise choropleth map which will demonstrate number of voters area by area e.g. map visualizing total number of voters, and number of male and female voters.
