# Data Analysis with LLMs

Applications that have LLMs at their core, can help us explore and understand a dataset.  This dataset could have one or possibly several related tables. 

We can provide information about the data in a few ways:
* as an image of the structure of the table(s): column names and possibly data types.  This could be a snapshot of the model view of a Power BI data model, or an entity relation diagram of a database, 
* as text: a list of tables and for each table, a list of the columns, or
* as data: for example, tabular data in CSV or Excel files

The LLM can then
* provide a summary of the data and pattern e.g. identify as a star-schema arrangement of tables and label each table as a fact or dimension table,
* suggest strengths, weakness and improvements to the data structure,
* suggest a list of questions that we can ask to understand more about the data, and 
* provide those questions in actionable form perhaps as SQL or Python code.

If data was provided, the LLM can:
* build a few charts to provide insights, 
* write and execute some code to analyse the data and show the results.

Some specific current examples of data analysis capabilities are:
* ChatGPT 4 can receive both text and images about data
* the ChatGPT Data Analyst plugin will read data files

## Exercise: Analyse the 'Patient Stay' dataset

Download the (fictitious) dataset for this example from [here](https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/PatientStay.csv). Have a look at the data and form your own opinions about how you would analyse it. Then start a new conversation with your LLM  using the prompts below as a starter.

_Prompt 1:_ Acts as a data analyst with knowledge of SQL. You have a dataset about patients admitted to a ward in a hospital.  It is available as a SQL table named `PatientStay`.  Each row in the table represents a patient admission.  The dataset contains the following columns.

- `PatientId` (int): The unique ID of the patient.
- `AdmittedDate` (date): The date on which the patient was admitted.
- `Hospital` (varchar): The name of the hospital.
- `Ward` (varchar): The name of the ward.
- `Tariff` (float): The cost to treat the patient.
- `Ethnicity` (varchar): The ethnicity of the patient e.g., White, Asian. For some rows this value is missing (null).

_Prompt 2:_ Suggest some data analysis questions that could be answered with this dataset.

_Prompt 3:_ Write a SQL statement to list the patients that were admitted to either "Guy's Hospital" or "St Georges".

_Prompt 4:_ Write a SQL statement to list the patients that were admitted between two dates


## Exercise: Analyse a dataset

Use the LLM to provide insights into a dataset.  Choose one of the following datasets below or any other public data that you prefer.

* [Titanic Passengers](<https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Titanic Data.xlsx>)
* A list of 32 American supercars from the 1970's [MT Cars](https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/mtcars.xlsx)
* [Bank Churn Data](https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Churn.csv)
* [Airports in Europe](https://zomalextrainingstorage.blob.core.windows.net/datasets/Airports/eu-airports.csv)
* Results from BBC's Saturday evening dancing competition in Autum 2023 [Strictly](<https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Strictly Data.xlsx>)


Some LLMs have capabilities to import a dataset e.g. ChatGPT Data Analyst.  If your LLM can import the dataset, 
* ask the LLM to provide insights, charts, and 
* _possibly_ show the Python code to create those charts.

If your LLM  cannot  import the dataset, describe the data structure (a one line description of the table: list the column names and possibly add a short description for each), and ask the LLM to
* describe the dataset,
* suggest ways that this data can be analysed,
* write SQL or Python code or Excel formulas to analyse or summarise the dataset.

In both cases, add follow-on questions, for example:
* how would we add a new column that combines X and Y?
* summarise the data: sum column X and group by column Y



