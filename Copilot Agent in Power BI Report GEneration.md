# Prompts for Copilot agent in Power BI

<img width="50%" height="50%" alt="image" src="https://github.com/user-attachments/assets/6598725b-bbe6-4072-87a5-2f41cb80197d" />

<img width="50%" height="50%" alt="LOGO_PowerBI" src="https://github.com/user-attachments/assets/e7ce32b1-936e-42be-8ba1-8b11e33f452c" />



## General summary prompt

```
Summarize the customer activities on this page, excluding "Unknown" which corresponds to logged time for internal projects, internal meetings, general admin, ...
```

## Magic Prompt

```
Fill this template for customer specified on this page filter, for the dates filtered in this page, using the Copilot Prompt suggested for each part. Do not change the titles. Use nice formatting. Don't put references to the source.

Title: Activity Report for <Customer Name>

Period covered: <month or dates covered in this activity report>

Executive Summary
Copilot prompt: Can you give me an executive summary about the activity for the customer <Customer Name> / <the selected customer>, and for the month(s) of <Month Name>, without the information about the Overhead and without any hours information, and without any references please ? Also, Provide more details on the specific actions taken please

Main tasks and projects
2.1 Tasks & Projects description

Copilot prompt: Source: the same customer. Context: the log notes represent tasks that were realized under specific projects. Can you try to group the tasks into global project titles [still without any references please] ?

2.2 Proposed status & follow-up table

Copilot prompt: Can you create a table with the above projects, and with a Title column containing the project name, a Description column containing a short description for the project, a Health column containing 3 smileys (one happy, one meh, one unhappy), a Progress column a Start date and an ETA (Estimated Time of Arrival) column ?

Note: An Excel companion with data validation can be generated if required.

Risks / Challenges
3.1 Current

Manually populate the below table if there are some risks that were not covered in the Logged notes:

Risk	Severity	Action taken	Status
3.2 Addressed in the activities

Copilot prompt: Can you identify the top 3 risks and challenges from the logged notes ?

Conclusion / Next Actions
Copilot prompt: Write a conclusion from the logged notes.

ANNEX - Activities Details

Copilot prompt: List all the logged notes in a table, with the following columns: Project Title, Logged Notes, Date using the exact precise dates from the source activity file
```

## https://word.cloud.microsoft Prompt:

```
Generate a nicely formatted report with the following text, including a table of contents at the beginning:

<Paste response from above prompt>
```
