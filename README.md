# kickstarter-analysis

## Overview of Project

###  Purpose of the project is to estimate success of considered campaigns in certain category in relation to start dates and funding goals. Provide conclusion of the analysis accompanied with visualized data.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Performing the analysis of theater category outcome based on launch date, was created pivot table reflecting following data: Patrant category and Year as a filter, Launch dates adjusted to months as rows, Outcomes as column labels and Count of Outcomes as a body of the table. Parant category was filtered for 'theater' only, Column Lables filter was set excluding 'live' column. Accordig received data was created a line chart [Theater_Outcomes_vs_Launch.png](https://github.com/andgerashchenko/kickstarter-analysis/blob/da4f395be3b7edae6fe0ef8cdd9d1e11a502cc12/Theater_Outcomes_vs_Launch.png). 
### Analysis of Outcomes Based on Goals
Outcomes Based on Goals table was built by splitting goal set of amounts in separate ranges, to distunguish the most effective project rela tively to requested funds. 12 rows of goal amount ranges was added to the table, as well as 7 columns reflecting number of successful, failed and canceled projects, its totals and persantages. In order to link corrcet data to needed cells of the table, 'CONTIFS' fofmula was used. This formula filter data by given criteria, here is example: '=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays")'. As a rasult numbers of outcomes were distributed between ranges of goal amounts. Then using these numbers and totals, persantages of outcomes were computed. The following chart was built based on the table [Outcomes_vs_Goals.png](https://github.com/andgerashchenko/kickstarter-analysis/blob/da4f395be3b7edae6fe0ef8cdd9d1e11a502cc12/Outcomes_vs_Goals.png)
### Challenges and Difficulties Encountered
During this proccess some steps were challengeable, such as splitting date into months and years and adding to different caregories of the pivot table. Also performing formulas for Outcomes Based on Goals table requiared extra attentiveness, just one misstake could skew the chart and effect conclutions.          
## Results

- Analizing the chart Outcomes based on Launch Date, we can see that the most successful months are May and June, also it correlates with "failed" line, which confirms the dynamics. Therefore summer months are better time for starting theater campaigns and end of the year is less preferable.    

- Outcomes based on Goals chart shows that "plays" with fewer goals are more successful. So conclusion is try not to overestimate the project, maybe use more data for analysis.   

- Analysing these two sets of data, we can determine when is the better time to start a project and how much outcome should be expected. However this date can be insufficient, because we used absolute values and didn't consider possible outliers and other statistical biases, which could infuance conclutions. 

- To reveal some other paterns of this data set, we can create a table using count of backers and pledged amount, then get average donation for each project. After that to make line chart with two graphs: avarage donation and count of backers and compare correlation of them. Discrepancy points will indicate outliers, where possibly was a single investor with much larger amount of donation, which can skew correct estimate of particular type of project.

