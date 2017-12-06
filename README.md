# Title: Did REAL Winner Win the 2017 World Series?

## Team Member(s): Kameron Wells

# Variables Used:
Houston Astros average runs per game
Houston Astros average runs given up by starting pitching  per game
Houston Astros average innings pitched by starter per game
Houston Astros average runs given up by relief pitching per game 
Los Angeles Dodgers average runs per game
Los Angeles Dodgers average runs given up by starting pitching  per game
Los Angeles Dodgers average innings pitched by starter per game
Los Angeles Dodgers average runs given up by relief pitching per game 
# Monte Carlo Simulation Scenario & Purpose: 
The World Series this year between the Astros and Dodgers was one of the exciting World Series of all time resulting in the Houston Astros winning their first World Series of all time over the Los Angeles Dodgers. The red hot Houston offense was facing the lights out Dodger pitching which meant one would have to break. My project using Monte Carlo simulation uses game simulations. 
For offense I will use a PERT simulation to give us the expected runs scored for both teams offensives that game
For pitching I am more specific in this approach by breaking this down by starters and relievers for a vareity of reasons; pitchers have the ball every play of the game while hitter will bat 3 or 4 times a game, starter wont go the complete game every time so relievers will come in and clean it up. I elected to not break relievers up because I found a stat that had bullpen runs allowed which accomidates for any combination of relievers used. Because I used starters/relievers I also will use a PERT for expected innings during that game my starter will go and then the relievers will finish it up.
Finally I add runs scored to the opponents runs allowed and divide by two to get the expected runs scored per game. I.e. if the Astros offense has enough "production" (simulated runs that game) to score 5 runs a game but the Dodgers pitching has enough "production" (simulated runs given up that game) to only give up 3 runs a game then it is assumed they will meet in the middle and the Astros will score 4 runs that game off Dodgers pitching. First to 4 wins that series wins that World Series simulation
***if the game goes 9 innings and is tied then the team with the (expected) better bullpen will win.
***if bullpens are even then it is assumed the better offense will score eventually. 

### Hypothesis before running the simulation: 
Houston Astros deserves to win the World Series.

### Simulation's variables of uncertainty
List and describe your simulation's variables of uncertainty (where you're using pseudo-random number generation). 
For each such variable, how did you decide the range and which probability distribution to use?  
Do you think it's a good representation of reality?

## Instructions on how to use the program:
Note this is a Juypter Notebook project so you will need to take proper protcol in order to run this function. The project is broken down into mutiple cells as my work progressed.

If you are looking at the first two boxs you are importing packages and writing a PERT function we used in class. 
The third cell is simple series simulation. 
The fourth cell is a Monte Carlo Simulation for runs allowed and runs given up by each team.
The fifth cell factors in runs given up by starting pitchers (per nine innings, how many innings they will go, and runs given up by the bullpen (per 9 innings),
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
