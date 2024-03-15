# Data Analysis with LLMs

Applications that have LLMs at their core, can help us explore and understand a dataset.  This dataset could have one or possibly several related tables. 

We can provide information about the data in a few ways:
*as an image of the structure of the table(s): column names and possibly data types.  This could be a snapshot of the model view of a Power BI data model, or an entity relation diagram of a database,
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
* CoPilot  - to do -
* Gemini  - to do -

## Using LLMs to assist with SQL and Python

LLMs are exceptionally good at helping us understand, learn, and write code.  SQL and Python are the two main languages for data analysis.  These LLMs, (wrapped in an application or user interface) are often called code-assistants.
Code assistants help in many ways:
* If we are writing a line of code, the assistant can suggest possible ways we want to complete that line or block of code.
* We can state our intent (what we want to do) in English (other human languages are available possibly to lesser extents) in a comment line and the assistant will write the code blow the comment.
* The assistant can review, explain, and add comments to existing code.
* The assistant can improve the code to a better standard and quality.
* If our code has generated an error, the assistant can explain why the error occurred, explain how to fix it and possibly fix it for us.

Examples of code assistants include:
* GitHub CoPilot:  Works with popular VSCode editor, popular especially for Python,
* CoPilot in Microsoft Fabric Python notebooks,
* (In beta currently), an assistant in Google Colab Python notebooks,
