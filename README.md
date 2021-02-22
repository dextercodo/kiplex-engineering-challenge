# kiplex-engineering-challenge


## Introduction
- This is the coding test for prospective KipleX engineers.
- This is a modified data analysis problem relating to racing cars on a speeding track.
- The data is unstructured.
- The data should not be changed.

### Purpose
- Primary purpose: to gauge the candidate’s problem solving skills.
- Secondary purpose: to gauge the candidate’s technical skills and competencies.
 
## Problem Statement
- F1 racing track has been divided into section (p_r_1, p_r_2, p_r_3 etc…). Each section is a 1km stretch.
- Certain sections of the track may contains hazards or un-even road causing traffic to slow down or even queue sometimes.
- Tracking devices were installed in the F1 cars to collect data while training for a race. And data were collected 1 week prior to the race
- The organizing company has approached you to have a look at the raw data and attempt to analyze it in order to improve the individual driver performance.
- Data is collected in the form of events. each event has a start timestamp and end timestamp.
- Event data are structured as follow:
    1. vehicle_1 started at p_r_1, on xxx time, while speeding, ended at p_r_1 at xxx time.
    2. vehicle_1 started at p_r_2, on xxxx time, while speeding, ended at p_r_2 at xxxx time.
    3. vehicle_1 started at p_r_3, on xxxxx time, while normal speed, ended at p_r_3 at xxxxx time.
- Multiple events can occur in the same section based on status as follow: 
    1. vehicle_1 started at p_r_1, on xxx time, while normal speed, ended at p_r_1 at xxx time.
    2. vehicle_1 started at p_r_1, on xxxx time, while speeding, ended at p_r_1 at xxxx time.
    3. vehicle_1 started at p_r_1, on xxxxx time, while stopped, ended at p_r_1 at xxxxx time.
- The F1 clubs management would like to analyse this data to understand how much time each F1 car spends in each section in order to optimise the race strategy. 
    - [benchmark] The best driver was able to complete 1 loop in 3 hours.
    - Individual club drivers' result would vary between 3-4 hours.

 
## Expected Solution
- The management is particularly looking to see the following:
    - Amount of time spent speeding per car at specific sections types that include ['p_d', 'p_h_a_d'].
    - Amount of time spent queuing per car at specific section types that include ['p_h', 'p_h_a', 'p_h_a_d', 'p_s', 'p_s_a'].
    - Amount of time spent idle per car at specific section types that include ['p_r'].
    - Average loop time per car.
- You’re expected to create an end-to-end solution that includes a database, a backend APIs, and a frontend web application to display the results.
- The solution should be functional.
- The solution should be object oriented, based on DRY and single responsibility principles.
- Provide comments in code to explain implementation.
- Your code should be readable, i.e. do not use naming such as "x" or "x_1" etc… instead, kindly provide meaningful naming such as "vehicle_speeding_time" or "point_accumulative_speeding_time". 
- Your solution should utilise a client-server pattern as follow:
    - Database to store and manipulate the data (such as MySQL/PostgreSQL/MongoDB)
    - Backend framework (such as RoR/Django/Phoenix/NestJs/BeeGo/Revel) with RESTful APIs
    - Frontend framework (such as Angular/React)
- Your solution should adhere to the following guidelines:
    - Frontend to display the data as is and not have and business logic. should allow the user to view the time in [seconds, minutes, hours] by choosing via a toggle or drop down list etc... 
    - All data aggregation/manipulation should happen at the backend or database layer (you’re free to chose)
Appearance is not critical, basic bootstrap is acceptable as long as there’s some form of styling (CSS)
Coding style is the primary factor for the assessment. 

## Instructions
- Clone this [repository](git@github.com:dextercodo/kiplex-engineering-challenge.git)
- Create a database and import the data from the CSV file.
    - You are free to chose a database of your preference (MySQL is preferred).
    - Table columns are as follow: 
```
[v_id, c_id, start_time, start_point, start_point_type, end_time, end_point, end_piont_type, status]
```
- You are free to aggregate and manipulate the data in whichever way you like, however the data should not be changed.
- Include your final SQL dump file in your solution.
- Solve the problem using the tools mentioned.
- Make a fork, and then create a PR for the fork when you are ready for answer submission!
- Notify dexter.karim@kiplex.com upon PR request with link to PR and demonstration of PR ownership.