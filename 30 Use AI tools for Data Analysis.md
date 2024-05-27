# Use AI Tools for Data Analysis and Coding

AI tools can help us explore, understand and visualise a dataset. We often will use a language such as SQL, Python or DAX (the data modelling and calculation language of Power BI) for our data analysis.  There is a specific section later in the course for each of these.


This dataset could have one or possibly several related tables. For best results, we provide information about the data in an initial scene-setting prompt.  We can do this in a few ways:
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

# AI Code assistenat / Pair Programmers 

AI Tools are exceptionally good at helping us understand, learn, and write code.  When these tools are embedded into our code editor, they are known as called code-assistants or pair-programmers.  They help in many ways:
* If we are writing a line of code, they can suggest possible ways we want to complete that line or block of code.
* We can state our intent (what we want to do) in English (other human languages are available possibly to lesser extents) in a comment line and they will write the code below the comment.
* They can review, explain, and add comments to existing code.
* They can improve the code to a better standard and quality.
* If our code has generated an error, they can explain why the error occurred, explain how to fix it and possibly fix it for us.

Examples of code assistants include:
* GitHub Copilot:  Works with popular (free) VSCode editor.  It is popular for Python and SQL.
* Copilot in Microsoft Fabric Python notebooks;
* (In beta currently), an assistant in Google Colab Python notebooks.


## Exercise: Analyse a dataset

Use an AI tool to provide insights into a dataset.  Choose one of the following datasets below or any other public data that you prefer.

* [Titanic Passengers](<https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Titanic Data.xlsx>)
* A list of 32 American supercars from the 1970's [MT Cars](https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/mtcars.xlsx)
* [Bank Churn Data](https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Churn.csv)
* [Airports in Europe](https://zomalextrainingstorage.blob.core.windows.net/datasets/Airports/eu-airports.csv)
* Results from BBC's Saturday evening dancing competition in Autum 2023 [Strictly](<https://zomalextrainingstorage.blob.core.windows.net/datasets/misc/Strictly Data.xlsx>)


Some AI tools have capabilities to import a dataset e.g. ChatGPT Data Analyst.  If your tool can import the dataset, 
* ask the LLM to provide insights, charts, and 
* _possibly_ show the Python code to create those charts.

If your AI tool  cannot  import the dataset, describe the data structure (a one line description of the table: list the column names and possibly add a short description for each), and prompt it to
* describe the dataset,
* suggest ways that this data can be analysed,
* write SQL or Python code or Excel formulas to analyse or summarise the dataset.

In both cases, add follow-on questions, for example:
* how would we add a new column that combines X and Y?
* summarise the data: sum column X and group by column Y
