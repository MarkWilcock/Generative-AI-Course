# Use AI tools to help with Excel Challenges

People who use Excel regularly appreciate that there are often challenges building Excel spreadsheets.  AI tools can help us become more productive with Excel in several ways. These include:
* get advice on how to perform an Excel task.  We can describe a problem in English to the AI tool and it will write the formulas required and explain how to apply (and possibly build an example spreadsheet);
* understand the formulas and functions Excel spreadsheet (one we may have inherited for example);
* understand how to use an Excel function (for example, choose good values for the arguments) or choose the appropriate function to use: e.g., is VLOOKUP or XLOOKUP better in a particular case?
* write Excel formulas; and 
* diagnose why Excel cell contains an error value e.g., #N/A, #NAME?, #NULL!, and suggest how to fix the formula or problem that caused it.

## Tutorial: Use an AI to help with Excel 

This exercise uses an example of a spreadsheet (not supplied) that contains Excel tables and uses Excel functions such as XLOOKUP. The prompt below are provided as suggested starter ideas.  Feel free to change or adapt these to suit your circumstances.  If you have your own spreadsheet, you may want to ask questions about the formulas in that.  

_Initial Prompt:_
Act as a helpful Excel expert.  Keep your answers brief unless I ask for more detail.

_Example prompts (to write a formula):_
Write an Excel formula to 
* add up values in cells C2 to C100.
* add up values in cells C2 to C100 when the corresponding value in the B column is "Alpha"
* to lookup the price of a banana in an Excel table named ShoppingList with columns Item and Price
* to extract all the text before the space character in a cell value
* give a list of unique items in the ShoppingList table

_Prompt (to explain a formula):_
Please explain what this formula does  
=XLOOKUP($G26, ItemsFinal[Fruit], ItemsFinal[Price])

_Prompt (to explain why a cell is showing an Excel error):_
=XLOOKUP($G28, ItemsFinal[Fruit], ItemsFinal[Price]) is a #N/A error.  Please explain why this error occurred and how to fix it.

_Prompt (a teaching example on some aspect of Excel):_

Explain the Excel XLOOKUP function with a few examples.

A follow-up question could be: Should I use the XLOOKUP or VLOOKUP function in my Excel spreadsheet?

## Tutorial: Use an AI to help summarise data in an Excel sheet

The [PatientStay spreadsheet](./Resources/PatientStay.xlsx) contains fictitious data about 44 patient hospital stays.  The data spans 4 London hospitals and 5 wards.  Patients are admitted for a few days in February and March 2024.  The columns are:
* PatientId
* AdmittedDate
* DischargeDate
* Hospital
* Ward
* Tariff
* Ethnicity

We would like help in writing formulas to summarise the data, for example:
* number of patients admitted to each hospital (and later the total tariff by hospital)
* number of patients admitted on each date
* the length of stay (in days) of each patient

Here are some suggested prompts to start your analysis.
* Act as an Excel expert.  The attached spreadsheet has data on patients stays in hospital.  Import the file and describe the data.
* How would I construct Excel formulas to find the number of patients admitted to each hospital
* Can you write and export this spreadsheet with these formulas
* Can you repeat that but use the UNIQUE function to generate the list of hospitals.
* Write a formula to calculate the length of stay for each patient.
* Is DATEDIF an Excel function?

## Tutorial: Use an AI to help with an Excel task (build a matrix of BMI values)

In Excel, I want to create a grid matrix  of values of body mass index (BMI) for a set of weights (60, 70, 80 100 Kg) on the row headers and  heights (1.6,1.7, 1.8, 2.0 metres) on the column headers.  The BMI formula is weight / (height * height).  How do I do this?

_Prompt: (to complete an Excel task, stack data)_

My spreadsheet has three tables named Jan, Feb and Mar. All three  tables have the same structure as in the example below.

| Date       | Category | Amount |
|------------|----------|--------|
| 13/01/2024 | Alpha    | 10     |
| 26/01/2024 | Bravo    | 20     |

Write an Excel formula to stack the data in these three tables into a combined table.

## Exercise: Use an AI to help with an Excel task (build a matrix of BMI values)

In Excel I have a column of text containing the full name of several people, in the format last name, title. othernames
for example:
> Braund, Mr. Owen Harris
> Cumings, Mrs. John Bradley (Florence Briggs Thayer)
> Heikkinen, Miss. Laina

I want to split these names up into three columns: lastname, title and other names.
This is the result I want based on the examples

|last name | title | other names                         |
|----------|-------|-------------------------------------|
|Braund    | Mr    |Owen Harris                          |
|Cumings   |Mrs    |John Bradley (Florence Briggs Thayer)|
|Heikkinen |Miss   |Laina                                |

