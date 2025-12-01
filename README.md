

<table style="width:100%; border-collapse:collapse; border:none;" border="0">
  <tr>
    <!-- Image Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%;">
      <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" />
    </td>
    <!-- Text Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%;">
      <strong>Welcome to aka.ms/CopilotActivityReporting</strong>
    </td>
  </tr>
</table>






# Generate an activity report for each customer (monthly, bi-monthly,...)

## Prerequisites

- you will need **your activity file (Excel or CSV)**. To have the best results in generating an activity report with Copilot, this CSV or Excel report should have at least the following columns:
  - ***Labor date***
  - **Engineer Name or Alias**, especially if several engineers share the same workbook to track their labor notes
  - ***Customer or Company Name***
  - ***Labor Notes***
  - Optionnally ***Logged Hours*** indicating how much labor the task took

 |Labor Date|Engineer Name or Alias|Customer or Company Name|Labor Notes|Logged Hours|
 |----------|-------------|------------------------|-----------|------------|

 Example:
 
 <img width="451" height="241" alt="image" src="https://github.com/user-attachments/assets/fd564080-bf08-47c2-95f5-f075b5a6d9ed" />

> Tip for good quick notes:
> Structure a few words in the form ***<Project Title/Name> - <Quick description of what you did in a few words>***

- and then you will need **the suggested prompts on this page**, but you can tweak them, use your own, the possibilities are endless !

## Step 1 - Upload your CSV / XLSX file

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
*No prompt here, just chose **Add work content**, chose the file and hit [Enter].*

<img width="435" height="202" alt="image" src="https://github.com/user-attachments/assets/beb8bb56-7f19-41bb-8be8-866d3ef77d72" />

And then chose your file:

<img width="327" height="201" alt="image" src="https://github.com/user-attachments/assets/a8a3295c-8d6f-40b9-9be1-b9139ff86934" />

Copilot will load it into the session (Copilot 365 will upload it in your Onedrive for Business drive), and you will have to validate as if you had put a prompt - but you will just have the file in the chat box:

<img width="466" height="172" alt="image" src="https://github.com/user-attachments/assets/166a9558-d151-4fcf-9945-d27bc0b9460b" />

You will need to wait a little bit that the file uploads to Onedrive (if you're using M365 Copilot App or chat) or to the Copilot chat session. Sometimes, copilot will then summarize the uploaded file and give info on the file content, sometimes not, depends on its mood - in the below example he chose not to do it without me asking for it:

<img width="442.5" height="231" alt="image" src="https://github.com/user-attachments/assets/6987548c-a6fb-450c-9ebe-91702a132946" />


## Step 2 - List the customers available in the uploaded file and the available period covered to shape Step 3 prompt

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
```
List the customers available in the uploaded file and the available period covered. For each customer, give me the sum of hours logged, and sort by the hours logged . If a customer name is "Unknown", that means it's overhead time. Please ignore it.
```

This can take some time. But once it finishes processing the data, you will have something looking like the below:

<img width="456.5" height="289.5" alt="image" src="https://github.com/user-attachments/assets/73882030-b73e-439d-928c-b9418bbf848c" />

And copy (CTRL+C) the customer name you want to fill the template with, to paste on the prompt on prompt ```<Customer_Name>``` placeholder on **Step 3** below.

## Step 3 - Tell Copilot which customer and what month(s) you will focus on

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
```
We will focus on the customer <Customer_Name>, and on the months of <Month 01>, <Month 02>, etc...
```

Example:

<img width="450" height="64" alt="image" src="https://github.com/user-attachments/assets/eedd9729-fb75-4b2a-a708-ec0fda5c929c" />


## Step 4 - Ask copilot to use a template you paste

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt] - copy the whole prompt below, no need to change customer name or period because we specified it on the *Step #3* prompt above** :

```
Fill this template for customer specified on the previous prompt, for the months specified in the previous prompt, using the Copilot Prompt suggested for each part. Do not change the titles. Context: the generated activity report will be for a Word document.

Title: Activity Report for <Customer Name>

Period covered: <month or dates covered in this activity report>

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

<img width="439" height="282" alt="image" src="https://github.com/user-attachments/assets/fce6e369-e2af-41d3-be2e-c8141b4a0ec8" />


## Step 5 - Generate a formatted Word document

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt] :**

```
Generate a formatted Word document.
```

Copilot will generate a Word document and give you a download link similar to the below:

<img width="318" height="354" alt="image" src="https://github.com/user-attachments/assets/10611e96-8b53-4e63-9cc1-2b324f9b7e52" />

... and Copilot even proposes to create an Excel companion file ! This AI tool is awesome 🥹

<img width="592" height="356" alt="image" src="https://github.com/user-attachments/assets/184d5010-af09-4487-bd39-e55bafa67b72" />


