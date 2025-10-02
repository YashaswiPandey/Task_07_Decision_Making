# Analysis of the Premier League 

To find the teams that have achieved great success or dissapointment over the past 30 years in the premier league, then identify the team that underperformed and how they can improve.

# Executive Summary

Data is the slowly taking an important role in the functioning of football clubs around the world, with key decisions now backed by thorough analysis of the data, this has led to a research in historical trends, player perfomance analysis, sports science to keep player fitness in check and to decide how to improve as a team on the whole.

This report contains the methods and data used to come up with recommendations and risk levels associated with them for a Premier League club that has underperformed keeping the ethical, reliable, reproducable results while trying to avoid any bias.  

Key finding found during this were :  

    1. Brentford scored more goals than 5 just teams above them.
    2. Brentford conceded more goals than the same teams.
    3. Brentfords defence was the main issue.

The recommended actions were:

    1. Provide defencive training to midfielders and attackers. Risk - high
    2. Provide extra training to defenders as a group along with goalkeeper to improve communication and teamwork. Risk - low
    3. Work on defensive transition for whole team so attackers and midfielder can work together with the defence. Risk - medium

# Background and Decision Question

This analysis is for the coaches of the Brentford football club which ended up underperforming in the 2023/24 season and provides recommendations for the decision question *"How to improve so we can win 2 more games next season"*.

# Data and Methods

The data was collected from [Kaggle](https://www.kaggle.com/datasets/evangower/english-premier-league-standings/data/)  and consists the final Premier League standing for the seasons between 1994 and 2024.  

The methods used consisted of using core python, pandas and polars for our analysis, then use LLM's to see hoe they answered and if they were able to extrapolate the same findings as we did with code.

# Findings

Questions of various difficulty were asked to the LLM's to check if they were able to answer progressively complex analytical questions based on structured data. These were:  

## Simple (direct)

    **1**
    > which team has finished at position 1 most number of times?

ChatGPT & DeepSeek
Both calculated Manchester United with 13 times

    **2**
    > which team has the best goal scoring record over a period of 3 years

ChatGPT & DeepSeek
Both calculated Manchester City with 303 goals between 2017-2019

    **3**
    > which team conceded the least goals over a period of 3 years

ChatGPT & DeepSeek
Both calculated Chelsea with 61 goals between 2005-2008

    **4**
    > which team had the worst goal scoring over a period of 3 years

ChatGPT & DeepSeek
Both calculated Crystal Palace with 116 goals<br>
After verifying with code, both got this answer wrong, when  asked why, they said they did not check for only consecutive years

    **5**
    > which team had the worst goal conceded over a period of 3 years

ChatGPT & DeepSeek
Both calculated West Brom with 196 goals between 2017-2019<br>
After verifying with code, both got this answer wrong, when  asked why, they said they did not check for only consecutive years

## Complex (Reasoning)

    **6**
    > which team deteriorated the most from 2023 to 2024 but avoided relegation

ChatGPT 

Identified Brentford as the team that detoriated the most as they dropped 7 positions  

DeepSeek

Identified Chelsea and Manchester United as the team that detoriated the most, DeepSeek reasoned that since they were higher up in the table their deteoriation was worse as they are expectd to be better.


    **7**
    > As a coach of Brentford, if I wanted to win two more games this coming season, should I focus on offense or defense and If so, why

ChatGPT and DeepSeek both identified the defense as the issue, this is because they conceded 65 goals and since their goals scored was better than teams in the bottom half of the table.

Code shows that Brentford scored more goals on average than 5 teams just above them, but ended up conceding more goals on average when compared, thus both correctly identified that Brentford should focus on defense.


    As we can see that both ChatGPT and DeepSeek can get easy calculations right but we need to use better wording when asking to solve complex problems.

# Recommendations

## Low Risk

    1. Provide extra training to defenders as a group along with goalkeeper to improve communication and teamwork.

    As they are the main line of defence and issue arising here could be disastrous and lead to more goals scored


    2. Have the attackers continue their attacking practice.
    
    This is because they are already scoring more goals than their immediate competition.


    3. Give the attackers added defensive workload depending on position.

    This is so that they can work on their positioning while defending and not impeding a player better capable of handling the play

## Medium Risk

    1. Work on defensive transition for whole team so attackers and midfielder can work together with the defence.

    This will get the team working as a whole and each player will understand their positioning and role during a certain phase much better.

    2. Have the midfielders train in both attacking and defensive practice depending on role and rotating later on.

    This is because midfielders play a crucial role in both phases of play and training both the phases will help them during transition of play.

## High Risk

    1. Provide defencive training to attackers.

    This is because during a match thats tied they can make a differnce by giving more numbers to the defence, but will take away time from attacking practice.


# Ethical/Legal concerns

Data Provenance - Data was sourced from Kaggle and no changes were made before any analysis was conducted

LLM Transparancy - All responses from both the LLM's were archived and are present in the appendix

Bias - As part of the project dependent on use of LLM's any bias present in themm could be reflected in the answers provided by them. When deciding which team I should focus on by asking question 6, i avoided deepseeks choice as selecting the team there could have introduced personal bias as I am a supporter of that team.

# Next Steps and Validation

The next steps and validation include - 
    
    1. Adding more data such as expected goals scored, expected goals conceded and other metrics that might improve the analysis by both human and LLM's.
    
    2. Getting feedback on the analysis by subject matter experts and refining the work further

    3. Track LLM responses to check for limitations and investigate root cause, keep validating answers with code
