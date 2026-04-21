# Prompts for Copilot agent in Power BI

<img width="10%" height="10%" alt="image" src="https://github.com/user-attachments/assets/6598725b-bbe6-4072-87a5-2f41cb80197d" />

<img width="10%" height="10%" alt="LOGO_PowerBI" src="https://github.com/user-attachments/assets/e7ce32b1-936e-42be-8ba1-8b11e33f452c" />

<table style="width:100%; border-collapse:collapse; border:none;" border="1">
  <tr>
        <!-- Text Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%; border:none;">
      <span style="font-size:32px; font-weight:bold;"><i>Click here for the prompt for Copilot inside Power BI<i></span> <br>
        <a href="https://github.com/SammyKrosoft/Copilot-Prompts-for-Activity-Reports/blob/main/Copilot%20Agent%20in%20Power%20BI%20Report%20GEneration.md">
          <img width="30%" height="30%" alt="Copilot in Power BI Logo 2" src="https://github.com/user-attachments/assets/979266ca-c866-4a7b-bfb2-b8dfb00f88f2">
        </a>
    </td>
    <!-- Text Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%; border:none;">
      <span style="font-size:32px; font-weight:bold;"><b>Welcome to aka.ms/CopilotActivityReporting<b></span>
    </td>
    <!-- Image Cell -->
    <td style="text-align:center; vertical-align:middle; width:50%; border:none;">
      <span style="font-size:32px; font-weight:bold;"><i>Click here to go back to the M365 Copilot walkthrough<i></span> <br>
      <a href="https://github.com/SammyKrosoft/Copilot-Prompts-for-Activity-Reports/blob/main/README.md">
      <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/0231166d-41cd-4130-8c24-44c12e0a47ce" />
      </a>
    </td>
  </tr>
</table>


## General summary prompt

```
Summarize the customer activities on this page, excluding "Unknown" which corresponds to logged time for internal projects, internal meetings, general admin, ...
```

## Magic Prompt

```
Fill this template for customer selected on this page, for the dates filtered in this page, using the Copilot Prompt suggested for each part. Do not change the titles. Use nice formatting. Don't put references to the source.

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
