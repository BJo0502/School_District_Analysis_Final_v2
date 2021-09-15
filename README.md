
# Module 4: PyCitySchools with Pandas

## Overview of the school district analysis

For the purpose of this Challenge, we are tasked to provide support to Maria, a chief data scientist who works for a city school system. Previously, we supported Maria by preparing the schools’ standardized test score data to be used for future trend and pattern analysis. Upon further a review, we have been informed that the data shows evidence of academic dishonesty so we most modify our data to not include the school and grade in question as the scores impact the total results for the district. We have been asked to repeat the district analysis without including Thomas High School’s 9th graders test results.

## Results: 

### How is the district summary affected?

Thomas High School (THS) is the 2nd highest performing school in the district. After removing the 9th grade results from our analysis, we can see that the overall district results decrease slightly with the exception of Average Reading; however, THS remains the 2nd highest performing school in the district. We notice that some of the results in the District Summary do not change such as the Total Schools and Total Budget. Since we only converted the 9th grade students' math and reading scores from THS to NaN, the Total schools and Total Budget results are not impacted. This makes sense since THS is still a school in the district and the current budget allocated to the school remains intact (at least for now). While we are not instructed to convert the Total Students column to NaN, it is best practice to display the change in student count for the sake of the District Summary since the input of this column directly impacts the rest of the statistical columns.
![DistrictSummary](https://user-images.githubusercontent.com/88041368/133296352-f8770519-00c0-4747-ae4e-791541e06147.png)
### How is the school summary affected?
### Math and reading scores by grade
![District_Analysis_Original](https://user-images.githubusercontent.com/88041368/133303703-9ce0ba87-bb9d-4d50-86e2-165b191a8571.png)
![District_Analysis_Modified](https://user-images.githubusercontent.com/88041368/133303701-2e20c711-841d-4430-9a76-65ada736cb4c.png)
*Note that Total Students for THS remains unchanged despite the removal of the scores from the analysis. This was done intentionally to display that the student counts were not changed to NaN values. Additionally, the Per Student Budget value is impacted by the total student count--ie: just because 9th grade results were removed does not mean the budget per student in 10th-12th grades has increased.*

After modifying our District Analysis we see that THS' results remain largely unimpacted in interms of overall ranking school performance; however, if we examine THS' modified results we can start to see the impact of removing it's 9th grade scores. All of the values decrease except the Average Reading Score (Avg Math: -.07, Avg Reading: +.05, % Passing Math: -.09, % Passing Reading: -.30, % Overall Passing: -.32). This makes sense when we look at the Average Math and Reading Scores per school, by grade. We can see that for math, THS' highest performing grade was 9th so removing these results from analysis would cause the Average Math, % Passing Math and the % Overall Passing to decrease. When we look at the Average Reading Scores per school, by grade we notice that THS' 9th grade was the 2nd lowest performing grade so removing it from our analysis causes the overall reading average to increase for THS. Since the % Passing Reading still decreases slightly despite the overall reading average increasing it's possible that the passing scores were higher in grades 10-12; however, a majority of the students that did not pass are also in grades 10-12.

![MathScoresByGrade](https://user-images.githubusercontent.com/88041368/133308024-09bdecff-58d9-4668-b8b1-342c81235d13.png)
![ReadingScoresByGrade](https://user-images.githubusercontent.com/88041368/133308027-b6984817-ffe2-4606-99ee-6f0ea135f733.png)

The slight increase in Average Reading Score and slight decrease in all other statistical fields is a trend that we see repeated when we visualize the data based on school spending, size, and type. If we format these data frames to only display 2 decimal places prior to comparing the original analysis to the modified results, it actually appears that the results for these data frames remain unchanged. By displaying the values prior to formatting we can see that our results have been impacted by the removal of THS' 9th grade results.


### Scores by school spending
*The top data frame is the original analysis and the bottom data frame are our modified results*
![ScoresBySchoolSize](https://user-images.githubusercontent.com/88041368/133309067-f7688271-db81-40ea-9072-0edc703a3b38.png)
### Scores by school size
*The top data frame is the original analysis and the bottom data frame are our modified results*
![ScoresBySchoolSpendingPerStudent](https://user-images.githubusercontent.com/88041368/133309069-56637b5f-387b-4b45-a9bf-e573f4cc1657.png)
### Scores by school type
*The top data frame is the original analysis and the bottom data frame are our modified results*
![ScoresBySchoolType](https://user-images.githubusercontent.com/88041368/133309071-a79ced28-2a7a-4811-ba5e-0a68480d776b.png)
## Summary
In summary, we can see that removing THS' 9th grade results impacted our analysis in the following ways:
Average Math Score dropped by .07,
Average Reading Score increased by .05,
% Passing Math decreased by -.09,
% Passing Reading decreased by -.30, and
% Overall Passing decreased by -.32. Evidence of academic dishonesty does not appear overtly present in the data itself.
  
