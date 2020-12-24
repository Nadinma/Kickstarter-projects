# Kickstarter-projects

#### High level description of project: as an idea to check if there is a way to predict (find a relationships) a successful project on kickstarter.

[More detailed scrypt](https://github.com/Nadinma/Kickstarter-projects/blob/main/kickstarter_capstone.ipynb)

### Intro

This project explored a dataset of about 378660 Kickstarter projects. Kickstarter is one of the popular crowdfunding platforms along with Indiegogo. The dataset was obtained from [Kaggel](https://www.kaggle.com/kemical/kickstarter-projects). The explored dataset contains data about projects from 2009 (when the platform was launched) up to January 2018. It has 7 projects from 1970 (they were dropped during exploration). 

I checked if there are duplicates in the dataset. From 378661 projects in the dataset there are not duplicates. 
Although the dataset was already cleaned, but some data still needed to be converted or seperated to get extra infomation. First I converted data from column "launched" (datetime data) to dtype('<M8[ns]'), which helped me to seperate days, months, years and hours when projects were launched. 

Here is some basic statistics / numbers about the dataset.

1. "ID"
2. "name"
3. "category"
4. "main_category"
5. "currency"
6. "deadline"
7. "goal"
8. "launched"
9. "pledged"
10. "state"
11. "backers"
12. "country"
13. "usd pledged"
14. "usd_pledged_real"
15. "usd_goal_real"

### Exploratory data analysis

### Dataset Numbers

Total goal - $13,767,829,762
Total amount pledged by backers - $3,297,997,512
Total amount pledged by backers to successful projects - $3,036,889,046
Total amount of money pledged by backers to failed projects is $261,108,466
Total number of projects - 331,675
Total number of successfully funded projects - 133,956
Proportion of completed projects which were successfully funded is: 40%
Mean project fundraising goal - $41,510
Mean amount pledged per project - $9,943
Mean amount pledged per successful project - $22,671
Mean amount pledged per failed project - $1,321
Mean number of backers per project - 116

#### There is about 378660 projects in dataset distributed through different categories. 
Film & Video |   63585
Music |           51918
Publishing      39874
Games           35231
Technology      32569
Design          30070
Art             28153
Food            24602
Fashion         22816
Theater         10913
Comics          10819
Photography     10779
Crafts           8809
Journalism       4755
Dance            3768

#### Here is what we know about the state of all the projects.

failed        197719
successful    133956
canceled       38779
undefined       3562
live            2799
suspended       1846

#### Distribution of projects by location - Countries of projects.
US      292627
GB       33672
CA       14756
AU        7839
DE        4171
N,0"      3797
FR        2939
IT        2878
NL        2868
ES        2276
SE        1757
MX        1752
NZ        1447
DK        1113
IE         811
CH         761
NO         708
HK         618
BE         617
AT         597
SG         555
LU          62
JP          40

#### Counted a number of successful project per category 
Music           24197
Film & Video    23623
Games           12518
Publishing      12300
Art             11510
Design          10550
Theater          6534
Technology       6434
Food             6085
Comics           5842
Fashion          5593
Photography      3305
Dance            2338
Crafts           2115
Journalism       1012

#### Counted overall projects per year 
2015    77300
2014    67745
2016    57184
2017    52200
2013    44851
2012    41165
2011    26237
2010    10519
2009     1329
2018      124
1970        7

#### Counted a number of successful project per year

2014    21107
2015    20971
2013    19415
2016    18766
2017    18462
2012    17892
2011    12171
2010     4593
2009      579

#### How Projects growth changed between 2009-2018
The graph below shows the number of projects launched on Kickstarter from 2009 to end of 2017 (2018 is not included). The first graph is showing growing numbers each year and the second graph is showing growing numbers within the same period of time, but each month.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen1.png)



The number of projects steadily grows from 2009 up to the middle of 2014. Projects started growing fast in 2014 and decreasing between 20015 and 2016.
On October 31 of 2012 Kickstarter opened projects based in the UK, followed by Canada in 2013, Australia and New Zealand and etc.
I am assuming a few reasons for such growth and then decrease: 1) looks like by 2014 Kickstarter reached the point where the wider audience is fully aware of its existence after step-by-step international launch. As a result it attracts more creators and backers. 2) Kickstarter added another four currencies to its platform and opened projects to five new countries: Netherlands, Sweden, Denmark, Norway and Ireland. 3) in 2014, Kickstarter made a lot of changes to their website, changes that making data collection not as straightforward as before. This factor might have impacted.

The bar charts below show failed vs successful projects between 2009 and 2018 (2018 is not included). We can see that starting from 2013 the number and of failed and successful projects start becoming even.

![] (https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen2.png)

Projects have more than two states (failed or successful). I am planning to drop other raws and plot only failed and successful projects below and in the futures graphs.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen4.png)


#### The difference between successful and failed projects

The graphs below show how various features differ between failed and successful projects.

The graphs below show how various features differ between failed and successful projects.

1. It looks like successful projects are having smaller goals - the median amount asked by successful projects is half almost of what failed projects are asking for.
2. There is a big difference in the median amount pledged per project, which is higher than the median amount requested. I am assuming that if projects meet their goal they attract more attention and as a result more funding.
3. There is a large difference between failed and successful in terms of amount pledged and the number of backers. I am assuming once potential supporters see that a project is picking up and doing well, they are willing to fund and be part of the future success.
4. Campaign length and the project name length doesn't differ much, campaigns are slightly shorter for successful projects. 

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen3.png)

#### Categories of projects launched and which are more successful
1. There are 15 project main categories (which are divided into more narrow categoris), where film & video is the most popular, followed by music, publishing, and games.
2. If we look at the median goal we can see that technology projects show the highest goals, followed by design, food, and games.
3. But we can see that technology projects have very low median pledged amount. Technology may ask for bigger goal (since innovations in tech are more expensive), also there is lot of competition from bigger companies (it involves not only actual technology, but also creative product design).
4. Design, dance, games, comics, and theatre projects get the highest funding based on info about median pledged amount.
5. We can see that in terms of median backers the most popular categories are dance, theatre, design, film&video, music, fashion, food, games and journalism, crafts and technology are the least popular (the reason might be their funding goals).
6. Comics and games are attracting the most amount of backers, but less amount pledged per backer.
7. Dance, design and film & video get more money per backer.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen5.png)

#### Projects origin
1. Most of the projects are coming from the US following by the UK. The number of US projects is much higher than from other countries. is six times more than projects from other countries.
2. If we look at the most amount of backers, pledged amount and median pledged Hong Kong is the most successful country.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen6.png)

#### Project Launch Weekday
1. Tuesday is the best day to launch a project. It is the most popular launch day, and there is the highest amount of successful projects launched on Tuesday. Tuesday is the most successful day in all categories - amoutn of backers, the highest median pledged per backer, and the highest median pledge amount.
2. Saturday and Sunday are the least popular days for any project activities.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen7.png)

#### Project Launch Month¶
1. The most popular months for project launch are September, October, November, and the least popular are July and January.
2. Fall is popular time for all projects activities and July and January are the least active months for all activities around projects success.
3. Median goal sizes are similar throughout the year.
4. The best month to launch in is October. It's demonstrating the highest median amount pledged per project, ine of the the highest amount of successful projects, the highest number of backers per project.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen8.png)

#### Launch Time
1. The most number of projects launched is between 4-6pm (GMT) - 8-10am PST.

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen9.png)

#### Campaign Length for Successful Projects
1. The shortest campaign length was 1 days and the longest campaign length was 92 days. 
2. Based on given stats we can see that the most number of successful projects have a campaign length of about 30 days. 

![](https://github.com/Nadinma/Kickstarter-projects/blob/main/images/screen10.png)

The dataset was not suited for hypothesis testing since it was all possible (population) data between 2009 and 2018. But potentially and as a further project development it's possible to continue working with additional data between 2018 and 2020. the mentioned data is avalaible, but needs more time to work with, which includes more data cleaning. 


