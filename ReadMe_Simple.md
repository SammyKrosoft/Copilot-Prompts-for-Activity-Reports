<table style="width:100%; border-collapse:collapse; border:none;" border="0">
  <tr>
    <!-- Image Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%; border:none;">
      <img width="100" height="100" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" />
    </td>
    <!-- Text Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%; border:none;">
      <span style="font-size:32px; font-weight:bold;"><b>Welcome to aka.ms/CopActRep</b><br><i>Shorter version of aka.ms/CopilotActivityReporting</i></span>
    </td>
  </tr>
</table>

> Note: a more verbose  version of this Walk-Through can be found on this link : [More verbose version of this Walk-Through](https://aka.ms/CopilotActivityReporting)

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
 
> Tip for good quick notes:
> Structure a few words in the form ***<Project Title/Name> - <Quick description of what you did in a few words>***

- and then you will need **the suggested prompts on this page**, but you can tweak them, use your own, the possibilities are endless !

## Step 1 - Upload your CSV / XLSX file

<img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
*No prompt here, just chose **Add work content**, chose the file and hit [Enter].*

Copilot will load it into the session (Copilot 365 will upload it in your Onedrive for Business drive), and you will have to validate as if you had put a prompt - but you will just have the file in the chat box.
You will need to wait a little bit that the file uploads to Onedrive (if you're using M365 Copilot App or chat) or to the Copilot chat session. Sometimes, copilot will then summarize the uploaded file and give info on the file content, sometimes not, depends on its mood.

## Step 2 - List the customers available in the uploaded file and the available period covered to shape Step 3 prompt

<img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
```
List the customers available in the uploaded file and the available period covered. For each customer, give me the sum of hours logged, and sort by the hours logged . If a customer name is "Unknown", that means it's overhead time. Please ignore it.
```

This can take some time.

And copy (CTRL+C) the customer name you want to fill the template with, to paste on the prompt on prompt ```<Customer_Name>``` placeholder on **Step 3** below.

## Step 3 - Tell Copilot which customer and what month(s) you will focus on

<img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt]**: 
```
We will focus on the customer <Customer_Name>, and on the months of <Month 01>, <Month 02>, etc...
```

## Step 4 - Ask copilot to use a template you paste

<img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt] - copy the whole prompt below, no need to change customer name or period because we specified it on the *Step #3* prompt above** :

```
Fill this template for customer specified on the previous prompt, for the months specified in the previous prompt, using the Copilot Prompt suggested for each part. Do not change the titles. Use nice formatting. Don't put references to the source. Context: the generated activity report will be for a Word document.

Title: Activity Report for <Customer Name>

Period covered: <month or dates covered in this activity report>

1. 	Executive Summary

Copilot prompt:	Can you give me an executive summary about the activity for the customer <Customer Name> / <the selected customer>, and for the month(s) of <Month Name>, without the information about the Overhead and without any hours information, and without any references please ? Also, Provide more details on the specific actions taken please


2. 	Main tasks and projects

2.1	Tasks & Projects description

Copilot prompt:	Source: the same customer. Context: the log notes represent tasks that were realized under specific projects. Can you try to group the tasks into global project titles \[still without any references please] ?

2.2	Proposed status & follow-up table

Copilot prompt:	Can you create a table with the above projects, and with a Title column containing the project name, a Description column containing a short description for the project, a Health column containing 3 smileys (one happy, one meh, one unhappy), a Progress column a Start date and an ETA (Estimated Time of Arrival) column ?

Note: An Excel companion with data validation can be generated if required.

3. 	Activities Summary

Copilot prompt:	Can you list all the logged notes in a table, with the following columns: Project Title, Logged Notes, Date using the exact precise dates from the source activity file?

Copilot prompt:	[Optional (to have an Excel companion for tasks / projects follow up)] - export this table to Excel and include data validation picklists for Health (🙂/😐/🙁) and Progress (Planned/In progress/In review/Completed).


4. 	Risks / Challenges

4.1	Current

Copilot prompt:	No prompts – manually populate the below table if needed – or delete this section.

Risk	Severity	Action taken	Status

4.2	Addressed in the activities

Copilot prompt:	Can you identify the top 3 risks and challenges from the logged notes ?
 

5. 	Conclusion / Next Actions

Copilot prompt:	Write a conclusion from the logged notes.

```

## Step 5 - Generate a formatted Word document

<img width="30" height="30" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" /> **[Prompt] :**

```
Generate the Word‑ready formatted version and produce the companion Excel file.
```

Copilot will generate a Word document and give you a download link.

... and Copilot even proposes to create an Excel companion file ! This AI tool is awesome 🥹


