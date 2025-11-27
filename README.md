<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" />


# Generate an activity report for each customer (monthly, bi-monthly,...)

## Prerequisites

- your activity file (Excel or CSV)
- thesuggested prompts on this page

## Step 1 - Upload your CSV / XLSX file

**Prompt**: no prompt here, just upload the file and hit [Enter]. Sometimes, copilot will then summarize the uploaded file and give info on the file content, sometimes not, depends on its mood.

<img width="896" height="437" alt="image" src="https://github.com/user-attachments/assets/df9d6c76-fa68-4bde-85fe-7303f1b8187b" />



## Step 2 - List the customers available in the uploaded file and the available period covered to shape Step 3 prompt

**Prompt**: ```List the customers available in the uploaded file and the available period covered. For each customer, give me the sum of hours logged, and sort by the hours logged . If a customer name is "Unknown", that means it's overhead time. Please ignore it.```

And copy (CTRL+C) the customer name you want to fill the template with to paste on the prompt on Step 3 below.

## Step 3 - Tell Copilot which customer and what month(s) you will focus on

**Prompt**: ```We will focus on the customer <Customer_Name>, and on the months of <Month 01>, <Month 02>, etc...```


## Step 4 - Ask copilot to use a template you paste

**Prompt - copy the whole prompt, replace customer name, and the months only on the *first line of the prompt*** :

```
Fill this template for customer specified on the previous prompt, for the months specified in the previous prompt, using the Copilot Prompt suggested for each part. Do not change the titles.


1\. 	Executive Summary

Copilot prompt:	Can you give me an executive summary about the activity for the customer <Customer Name> / <the selected customer>, and for the month(s) of <Month Name>, without the information about the Overhead and without any hours information, and without any references please ?

Copilot prompt	\[Optional] - Provide more details on the specific actions taken
 

2\. 	Main tasks and projects

2.1	Tasks \& Projects description

Copilot prompt:	Source: the same customer. Context: the log notes represent tasks that were realized under specific projects. Can you try to group the tasks into global project titles \[still without any references please] ?

2.2	Proposed status \& follow-up table

Copilot prompt:	Can you create a table with the above projects, and with a Title column containing the project name, a Description column containing a short description for the project, a Health column containing 3 smileys (one happy, one meh, one unhappy), a Progress column a Start date and an ETA (Estimated Time of Arrival) column ?


3\. 	Activities Summary

Copilot prompt:	Can you list all the logged notes in a table, with the following columns: Project Title, Logged Notes, Date using the exact precise dates from the source activity file?

Copilot prompt:	\[Optional (to have an Excel companion for tasks / projects follow up)] - export this table to Excel and include data validation picklists for Health (🙂/😐/🙁) and Progress (Planned/In progress/In review/Completed).


4\. 	Risks / Challenges

4.1	Current

Copilot prompt:	No prompts – manually populate the below table if needed – or delete this section.

Risk	Severity	Action taken	Status

4.2	Addressed in the activities

Copilot prompt:	Can you identify the top 3 risks and challenges from the logged notes ?
 

5\. 	Conclusion / Next Actions

Copilot prompt:	Can you write a conclusion from the logged notes ?

```
