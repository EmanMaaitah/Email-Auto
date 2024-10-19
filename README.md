# OBJECTIVE
The idea of ​​this project is to take job candidates’ data from an Excel sheet and send a message to whoever is accepted for the job.And send another message to those who did not accept.
## MANUALLY
Open an Excel file and look at who is accepted for the job and send a different formula for those who are not accepted.
# TECHNICAL REQUIREMENTS

## Use Gmail
1) [Use Gmail](https://docs.uipath.com/activities/other/latest/productivity%22/gmail-application-card)
2) [Send Email](https://docs.uipath.com/activities/other/latest/productivity/send-mail-x)
## Using Excel Activities
1) [Excel Process Scope](https://docs.uipath.com/activities/other/latest/productivity/excel-process-scope-x)
2) [Use Excel File](https://docs.uipath.com/activities/other/latest/productivity/excel-application-card)
3) [Read Range](https://docs.uipath.com/activities/other/latest/productivity/excel-read-range)

## Using Data Table Activities
1) [Output Data Table](https://docs.uipath.com/activities/other/latest/workflow/output-data-table)

   
# PROCEDURES
1) Inserts use excel scope>Use Excel File, enter the file name in the box "Hiring Proccess.xlsx"
   
   ![image](https://github.com/user-attachments/assets/bc2caaf9-858f-4219-ad35-852dce2f498e)

 2) Read Range activity, inside the range select the sheet and save it in dt_candidate variable

   ![image](https://github.com/user-attachments/assets/cd0e82cc-51d8-4190-8a6c-b4c056cedb1b)
  

 3) Output Data Table: Change the type of variable through the properties panel and save it in data variable

   ![image](https://github.com/user-attachments/assets/dbb239be-f41f-431b-a6a9-bb976b72e95a)

   .
   ![image](https://github.com/user-attachments/assets/8d96dcc1-3740-47b6-94a5-aeb4e6aaad50)


 4) Use Message Box activity

   ![image](https://github.com/user-attachments/assets/2487095b-4e1a-4503-b6d1-53dc604ec29d)

 5) Use Gmail activity in the Account field Enter your email address and connect it to your account


   ![image](https://github.com/user-attachments/assets/437346d6-8c62-46de-b7b8-f8d1da44ea57)
   

 6) In the do scope put For Each Row in Data Table activity

    ![image](https://github.com/user-attachments/assets/7f8e14fc-e92a-4683-a648-689f4faf8a0b)

 7) Inside the For Each > Use If activity, then select the condition: CurrentRow(2).ToString="Accepted"

    ![image](https://github.com/user-attachments/assets/1f99da0c-eb83-40dc-ab0a-31e8b1a4c237)




 8) Inside the then action put send email activity > Inside the account field add Gmail variable> in the field To CurrentRow("Email").ToString

    
    .
    ![image](https://github.com/user-attachments/assets/77983a50-da40-4486-ad7a-f906fe83606c)

    .
    ![image](https://github.com/user-attachments/assets/9bae9061-01cd-4d87-903d-51d1ed4471f9)


# Results

I have put my email in the suggested emails, In order to ensure that the email is sent.

To watch the robot run and the results, [click here](https://drive.google.com/file/d/15ezxrGKx97KdUWz3Ak8kDC28EXNadO1I/view?usp=drive_link)

