# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

## Gabriel Choo, SG DSI 14

### Problem Statement
The participation rate of ACT has decreased from year 2017 to 2018, in contrast to SAT which increases from year 2017 to 2018. In order to boost it's market share in the various states, what strategies can be implemented to encourage the graduates of that state to take the ACT college admission test?

### Executive Summary

The objective of this report is to describe and infer our study of the two main standardized test used for college admission in the United States and recommend how the college board might increase participation amongst the graduating student in the state.

The study included a detailed look at the aggregate scores and participation rate of each standardized test, ACT and SAT for year 2017 and 2018.

It has been observed the participation rate is greatly influenced by the state decisions to make either one of the standardized test a mandatory for high school graduates. By standardizing on one test, it is proven that the graduates score is much constant as students are more prepared for the test. In one of the analysis, the drop in mean and median score for SAT 2017 and SAT 2018 compared to ACT score shows that the sudden change in test (e.g. from ACT to SAT) impacted the graduate's total score. It might be due to the fact the state student has been following the specific test syllabus since they joined the school hence a change in test might be disadvantage to them as the subject and test framework might be different.

In order to increase the participation rates, the college board can consider incorporate both of the subject and test framework into the school syllabus itself so that graduates can be familiarize with the both test. With that they can allow the graduates to choose which test (or both) they are more comfortable or confident in, instead of restricting them to a mandatory one. In addition by eliminating barriers to the test, like subsidizing the test cost and offering the graduates greater flexibility to take the exams on weekdays and weekends, graduates that are less fortunate will be able to participate in any of the test.


### Data

For this project, we are given two provided datasets:
- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)

You can see the source for 2017 data:
- [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
- [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)

You can see the source for 2018 data:
- [here](https://reports.collegeboard.org/sat-suite-program-results/state-results).
- [here](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)

These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017 and 2018.

### Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---|---|:---|
|**state**|*object*|Final|The states in the United States of America
|**act_part**|*float*|ACT 2017|The percent of the graduates tested (units percent to two decimal places 0.98 means 98%)
|**act_eng**|*float*|ACT 2017|The average score of the language on a scale of 1-36
|**act_math**|*float*|ACT 2017|The average score of the language on a scale of 1-36
|**act_read**|*float*|ACT 2017|The average score of the language on a scale of 1-36
|**act_sci**|*float*|ACT 2017|The average score of the language on a scale of 1-36
|**act_comp**|*float*|ACT 2017|The average composite score of all the language on a scale of 1-36
|**sat_part**|*float*|SAT 2017|The percent of the graduates tested (units percent to two decimal places 0.98 means 98%)
|**sat_ebrw**|*int*|SAT 2017|The score of evidence-based reading and writing on a scale of 200-800
|**sat_math**|*int*|SAT 2017|The score of math on a scale of 200-800
|**sat_total**|*int*|SAT 2017|The total score of all the languages on a scale of 400-1600
|**act18_part**|*float*|ACT 2018|The percent of the graduates tested (units percent to two decimal places 0.98 means 98%)
|**act18_eng**|*float*|ACT 2018|The average score of the language on a scale of 1-36
|**act18_math**|*float*|ACT 2018|The average score of the language on a scale of 1-36
|**act18_read**|*float*|ACT 2018|The average score of the language on a scale of 1-36
|**act18_sci**|*float*|ACT 2018|The average score of the language on a scale of 1-36
|**act18_comp**|*float*|ACT 2018|The average composite score of all the language on a scale of 1-36
|**sat18_part**|*float*|SAT 2018|The percent of the graduates tested (units percent to two decimal places 0.98 means 98%)
|**sat18_ebrw**|*int*|SAT 2018|The score of evidence-based reading and writing on a scale of 200-800
|**sat18_math**|*int*|SAT 2018|The score of math on a scale of 200-800
|**sat18_total**|*int*|SAT 2018|The total score of all the languages on a scale of 400-1600
