# Use AI Tools for Data Analysis

AI tools can help us explore, understand and visualise a dataset.  For best results, we provide information about the data in an initial scene-setting prompt.  We can do this in a few ways:
* as a description of the stucture: the table name(s) and a list of column names.  If we want to be thorough, we can also include the  descriptions of each column (data type, whethere nullable, the set of valid values if appropriate), but this usually is not necessary.
* with some AI tools we can upload the data file - it is often better if this is a CSV rather than an Excel file.
* if we can't upload the data file, copy and paste the data, or at least the column headers and a few represenantive rows into the prompt.
* as an image of the structure of the table(s): column names and possibly data types.  This could be a snapshot of the model view of a Power BI data model, or an entity relation diagram of a database, 

The AI can then
* provide a summary of the data and pattern e.g. identify as a star-schema arrangement of tables and label each table as a fact or dimension table,
* suggest strengths, weakness and improvements to the data structure,
* suggest a list of questions that we can ask to understand more about the data, and 
* provide those questions in actionable form perhaps as SQL or Python code.
* if data was provided, the AI can analyse and summarise the data and build a few charts to provide insights.

After the initial prompt, we can prompt with follow-on questions, for example:
* how would we add a new column that combines X and Y?
* summarise the data: sum column X and group by column Y
* what are the factors that influence the values in column Z?

Note: data professionals will often use a language such as SQL, Python or DAX (the data modelling and calculation language of Power BI) for our data analysis.  There is a specific section later in the course for each of these.

# Tutorial - Analyse NHS England Outpatient Activity

We will use an AI tool to analyse the number of outpatient appointments in England over the past several years by outcome (attended, did not attend etc). The data is in a CSV file - download from [here](./Resources/NHS%20HES%20Outpatient%20Appointments%20England%20By%20Year%20And%20Type.csv) and have a look at it.  The original source data is from NHS Digital [here](https://digital.nhs.uk/data-and-information/publications/statistical/hospital-outpatient-activity/2022-23).

Suggested Prompts
* Describe the attached dataset _(Don't forget to attach the file)_
* Show attendance trends over the years.
* What is the trend in the percentage of cancellations?
* Calculate the percentage of cancellations as the 'Patient Calculations' column divided by the year total.  Please revise the calculation and chart.
* Why did this dip in the 2020-21 year?
* Are there any other insights available from the data?

<!--
## Exercise - Analyse Airports in Europe

[Airports in Europe](https://zomalextrainingstorage.blob.core.windows.net/datasets/Airports/eu-airports.csv)

-->

