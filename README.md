# Powerlifting Competition Analysis
## Tableau Dashboard: https://public.tableau.com/app/profile/charlie.tran3526/viz/uspa/SummaryDashboard

## Goal: 
Implement webscraping via Python's BeautifulSoup & Request libraries to generate a robust dataset that consists of powerlifting competition data for every competition for the USPA & USAPL federations. Website to scrape: https://www.openpowerlifting.org/. Visualize data in a Tableau dashboard that showcases the rising popularity of powerlifting as a sport for the top 2 federations in the U.S, the strength trends year over year and a way to show individiual lifters where they match up against their competition. 

## Data
Column Name| Details | 
---|---|
Lifter Name| The competitors first and last name |
Place | What place did the lifter achieve|
Sex | Sex of lifter |
Age | Age of the lifter |
Equip | Details if the lifter competed in the raw or equipped category|
Weight Class | Weight class of the lifter in KGs |
Weight (KG) | Weight of lifter in KGs |
Squat (KG) | Best squat for the lifter at that meet in KGs|
Bench (KG) | Best bench for the lifter at that meet in KGs |
Deadlift (KG) | Best deadlift for the lifter at that meet in KGs |
Total (KG) | Best total for the lifter at that meet in KGs |
Weight (LB) | Weight of lifter in LBs |
Squat (LB) | Best squat for the lifter at that meet in LBs|
Bench (LB) | Best bench for the lifter at that meet in LBs |
Deadlift (LB) | Best deadlift for the lifter at that meet in LBs |
Total (LB) | Best total for the lifter at that meet in LBs |
Dots | Dots achieved by the lifter at that meet |
Country | What country did the competition take place|
State | What state did the comp. take place |
Date | What date did the comp. take place |
YM | Truncated date to the year-month |
Number of Lifters | How many total lifters competed at the meet |
Competition | Competition Name|
Age Division | What age division did the lifter compete in |
Division Category | What division category did the lifter compete in|
Classification | What classification category did the lifter achieve |
Federation | What federation did this competition take place in |
Date Refreshed | Last refresh date of the data |

## Analysis
The overall audience I wanted my analysis to cater to was for powerlifting fanatics/enthusiasts and for the powerlifting federation officials/staff members. In my Tableau dashboard, there are several tabs that serve different purposes:
1. <b> Summary Dashboard </b>: Used to show basic summary statistics such as total number of competitions, total number of lifters, total number of cities etc. Shows various graphs that highlight distributions of different features. 
2. Strength Trends: Time series analysis of year over year strength trends through graphs of average totals, squats, bench and dealifts of lifters over time with the ability to filter by gender, age division, weight class, age, division category, etc. In figure 1, I filtered the data to visualize the 95th percentile of totals and the various lifts, chose the 67.5 KG weight class, full-power division category, open age-division, lifters in between the ages of 17-38 and excluded lifters who DQ'd or were a no show. We can see that for this specific subset of lifters, there has been an increase trend of strength to be in the 95th percentile of lifters (top 5%) across all lifts.
3. Popularity Dashboard: Time series analysis of the year over year growth of popularity of a specific powerlifting federation for total members, new members, number of meets and number of new cities. Figure 2 shows Tableau's built in forecasting tool I used to create a 3 year forecast for the features I just mentioned and also shows choropleth maps that summarizes the popularity of a state. The map corresponds to a ratio of the number of competitions the state has hosted divided by either the total number of lifters, or total number of unique lifters or both. This is useful in that a high ratio when dividing by total lifters tells us that there a lot of lifters who compete per meet. However, you have to control for how many competitions that state has hosted since that can skew the ratio. Therefore, if you see two states that have hosted a similar number of competitions, but one state has a significantly higher ratio, that tells you that more lifters come out to compete per competition which a staff member may want to investiate into as to why, and how they can bring up the number of lifters for the other states because that generates more revenue. On the other hand, a high ratio when dividing by unique number of lifters tells us that there are many unique lifters who compete in that state per competition. Similar to above, when comparing states with similar number of competitions, a staff member may want to investigate into the state with the higher ratio because they're able to bring in more new members which is a sign of popularity and growth.
4. Lifter Dashboard: A fun tab for competitiors to look up their name and see their performance highlights. Figure 3 shows an example for myself and my highlights from my 2 meets in the USPA showcasing my improvements from meet to meet, my best stats and where I rank among my peers. 
5. Classification Standards: This was actually a request from the USPA President Steve Denison and VP Mike Tronske when I presented him the Dashboard via email.They wanted to see a distribution curve based on USPA member DOT scores vs. the classification standards that USPA uses on their calculator. https://uspa.net/upcoming-events/#calculator. They believed it would be useful in determining what % of members are lifting within each classification and help determine whether the qualification requirements should be changed for future events such as Nationals, North American Championships, and IPL Worlds. (Figure 4)

Figure 1.
![Screenshot (325)](https://github.com/ctran2320/powerlifting/assets/133697095/08ab6013-608b-4c3b-b010-7a57804438bc)
Figure 2. 
![Screenshot (326)](https://github.com/ctran2320/powerlifting/assets/133697095/f8c42129-9ee8-42b9-867a-b63036509a55)
Figure 3.
![Screenshot (331)](https://github.com/ctran2320/powerlifting/assets/133697095/0fafa90c-5725-404e-844f-ac898640c342)
Figure 4. 
![Screenshot (328)](https://github.com/ctran2320/powerlifting/assets/133697095/8f1dbf63-6e94-41ec-bf15-dd8227e1fdaa)



## Future Work
