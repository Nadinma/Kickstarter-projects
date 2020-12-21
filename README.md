# Kickstarter-projects

#### High level description of project: as an idea to check if there is a way to predict (find a relationships) a successful project on kickstarter.

### Intro

This project explored a dataset of about 378660 Kickstarter projects. Kickstarter is one of the popular crowdfunding platforms along with Indiegogo. The dataset was obtained from https://www.kaggle.com/kemical/kickstarter-projects. The explored dataset contains data about projects from 2009 (when the platform was launched) up to January 2018. It has a few projects from 1970 (they were dropped during exploration). 

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
