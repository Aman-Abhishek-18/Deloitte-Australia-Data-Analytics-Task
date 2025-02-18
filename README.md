# Deloitte-Australia-Data-Analytics-Task
Here's Deloitte Australia's Data Analytics Simulation, focusing on data analysis, forensic tech, Tableau dashboards, and Excel insights.

## Here is the background information on task 1 :

Using a data unification algorithm, the tech team at our client, Daikibo, has converted all telemetry data collected from its 4 factories:
• Daikibo Factory Meiyo (Tokyo, Japan)
• Daikibo Factory Seiko (Osaka, Japan) 
• Daikibo Berlin (Berlin, Germany) 
• Daikibo Shenzhen (Shenzhen, China)

Each location has 9 types of machines, sending a message every 10 mins. Daikibo has been collecting this data for one month (May 2021) and they've shared this data in the form of a single JSON file. 

The reason the client wanted to collect telemetry was to answer 2 questions: 

1. In which location did machines break the most? 
2. What are the machines that broke most often in that location?

SOLUTION :

Step 1: Import data into Tableau
![image](https://github.com/user-attachments/assets/32ac3934-b45f-472f-ad0b-513879d13a7e)


Step 2: Create Calculated Field Under Measure Names List (Unhealthy)
![image](https://github.com/user-attachments/assets/860226ef-b066-4016-ac7f-92ab45782c63)


This calculated measure will help to learn how long was the down time of different pieces of manufacturing processes.
Since messages are sent every 10 min, we set this measure to 10 for every unhealthy status received.

![image](https://github.com/user-attachments/assets/b57e9298-691e-4d2b-8f37-0572a6e56f3c)

Step 3 : Create a Downtime Per Factory
![image](https://github.com/user-attachments/assets/dcef753c-95e7-4a87-b657-b5c21e8dbad3)

Step 4 : Create a Downtime Per Machine
![image](https://github.com/user-attachments/assets/8c698988-ab67-4865-bb7b-87cfe5f932c2)

Step 5 : Create a Dashboard using both Sheets (step 3 & 4) and click the filter/funnel icon at the top right of the sheet 1 i.e. Step 3 <br>
Now based on the selected Factory, required results are appearing.

![image](https://github.com/user-attachments/assets/18c87df1-a2d1-47a6-9e8d-b0c8ac814115)



<br>
<br>

## Here is the background information on task 2 :

Forensic technology 

Here is the background information on task 2 :

After a worrisome number of internal complaints about gender inequality in terms of salary, Daikibo Industrials wants us to help them investigate. 

The Forensic Tech team has built an algorithm to quantify "level of gender pay equality" for most job roles within the company, in all company locations. Our Forensics lead thinks it would be a great idea for you to finish the job.

Excel file containing 3 columns: 
1. Factory 
2. Job Role 
3. Equality Score (integer; ranging between -100 and +100; O is ideal) 

Here is your task: • Create a 4th column (Equality class), classifying the equality score into 3 types: • Fair (+-10) • Unfair (<-10 AND >10) • Highly Discriminative (<-20 AND >20) 

Examples:
 • 6 → Fair
 • -9 → Unfair
 • -30 → Highlv Discriminative

 SOLUTION :

 Step 1 : Add =IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative")) in the 4th column and drag it till end
<br>
<br>
<br>
 ![image](https://github.com/user-attachments/assets/c8b9003e-1342-4fe4-8425-bdb10e33da64)




