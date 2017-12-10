# Title: Did REAL Winner Win the 2017 World Series?

## Team Member(s): Kameron Wells

# Monte Carlo Simulation Scenario & Purpose: 
The World Series this year between the Houston Astros and Los Angeles Dodgers was one of the most exciting World Series of all time resulting in the Houston Astros winning their first World Series of all time over the Los Angeles Dodgers. The red hot Houston offense was facing the lights out Dodger pitching which meant one would have to break. My project using Monte Carlo simulation uses game simulations:

For offense I will use a PERT simulation to give us the "production" (expected runs scored for both teams offensives that game)

For pitching I am more specific in this approach by breaking this down by starters and relievers. I am more specific for a vareity of reasons; pitchers have the ball every play of the game while individual hitters will bat 3 or 4 times a game, starter wont go the complete game every time so relievers will come in and finish most games. I elected to not break relievers up because I found a stat on ESPN that had bullpen runs allowed which accomidates for any combination of relievers used. Because I used starters/relievers I also will use a PERT for expected innings during that game my starter will go and then the relievers will finish it up.

Finally I add one teams runs scored to the opponents runs allowed and divide by two to get the expected runs scored per game. 

I.e. if the Astros offense has enough "production" (simulated runs that game) to score 5 runs a game but the Dodgers pitching has enough "production" (simulated runs given up that game) to only give up 3 runs a game then it is assumed they will meet in the middle and the Astros will score 4 runs that game off Dodgers pitching. First to 4 wins that series wins that World Series simulation

*if the game goes 9 innings and is tied then the team with the (expected) better bullpen will win because it is assumed the better bullpen will hold the other team off long enough to score.*

*if bullpens are even in expected runs per game then it is assumed the better offense will score eventually. *

**I elected to do it in this manner because when I left it as "expected runs scored" that would account for any variation of the lineup that the team could configure so I didnt have to account for pinch hitters / designated hitter / spot in the order/ etc. management. But a starting pitcher is one player and has such an impacts on the game I did elect to make then each an individual entity while relievers were left as a whole (like hitters) to account for any possbile combination of relievers. 
I elected to leave it as starters vs relievers apperances (2 entity simulations) as opposed to a 9 inning game simulation (9+ entity simulations) because the only way to make a true 9 inning simulation would be to have hitters included because of different skilled hitter hit in different places of the order so to make it a fair simulation I left it as pitchers (2 entites) and hitters (1 entity) **

### Hypothesis before running the simulation: 
Houston Astros deserves to win the World Series.

### Simulation's variables of uncertainty
Houston Astros average runs per game
Houston Astros average runs given up by starting pitching  per game
Houston Astros average innings pitched by starter per game
Houston Astros average runs given up by relief pitching per game 
Los Angeles Dodgers average runs per game
Los Angeles Dodgers average runs given up by starting pitching  per game
Los Angeles Dodgers average innings pitched by starter per game
Los Angeles Dodgers average runs given up by relief pitching per game 

All will be using a PERT simulation because that will give us the distrubution wed for runs scored factoring the the min(0,0) for each team and max (19, 14) runs scored in a game, also runs given up in a game min (0,0) and max (13,13) for each team  and finally it is also a good distrubtion for pitching innings with a min (0) and max (9) innings pitched ranges.

## Instructions on how to use the program:
Note this is a Juypter Notebook project so you will need to take proper protcol in order to run this function. The project is broken down into mutiple cells as my work progressed.

If you are looking at the first two boxs you are importing packages and writing a PERT function we used in class. 

The third cell is simple series simulation. 

The fourth cell is a Monte Carlo Simulation for runs allowed and runs given up by each team.

The fifth cell factors in runs given up by starting pitchers (per nine innings, how many innings they will go, and runs given up by the 
bullpen (per 9 innings),

The sixth cell is the same as the fifth cell but rounds all the numbers (because you cant given up .5 runs in an inning)

And lastly the 7th cell (which is the rough draft final version of the project) does the same as the sixth but uses a PERT distrubtion because it will be more accurate that a expectation than a normal distrubtion.

## Sources Used:
http://www.espn.com/mlb/stats/team/_/stat/batting/sort/runs/order/true
http://www.espn.com/mlb/stats/team/_/stat/pitching
https://espn.go.com/mlb/stats/team/_/stat/pitching/split/128
https://www.foxsports.com/mlb/los-angeles-dodgers-team-stats?season=2017&category=PITCHING&group=1&time=0
https://www.foxsports.com/mlb/houston-astros-team-stats?season=2017&category=PITCHING&group=1&time=0
https://www.baseball-reference.com/teams/LAD/2017-schedule-scores.shtml
https://www.baseball-reference.com/teams/HOU/2017-schedule-scores.shtml
