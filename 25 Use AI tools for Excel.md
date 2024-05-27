# Use AI tools to help with Excel Challenges

People who use Excel regularly appreciate that there are often challenges building Excel spreadsheets.  
AI tools can help us become more productive with Excel in several ways. These include:
* get advice on how to perform an Excel task.  We can describe a problem in English to the AI tool and it will write the formulas required and explain how to apply (and possibly build an example spreadsheet);
* understand the formulas and functions Excel spreadsheet (one we may have inherited for example);
* understand how to use an Excel function (for example, choose good values for the arguments) or choose the appropriate function to use: e.g., is VLOOKUP or XLOOKUP better in a particular case?
* write Excel formulas; and 
* diagnose why Excel cell contains an error value e.g., #N/A, #NAME?, #NULL!, and suggest how to fix the formula or problem that caused it.

## Exercise: Use an AI to help with Excel 

This exercise uses an example of a spreadsheet (not supplied) that contains Excel tables and uses Excel functions such as XLOOKUP. The prompt below are provided as suggested starter ideas.  Feel free to change or adapt these to suiot your circumstances.  If you have your own spreadsheet, you may want to ask questions about the formulas in that.

_Initial Prompt:_
Act as a helpful Excel expert.  Keep your answers brief unless I ask for more detail.

_Prompt (to explain a formula):_
Please explain what this formula does  
=XLOOKUP($G26, ItemsFinal[Fruit], ItemsFinal[Price])

_Prompt (to explain why a cell is showing an Excel error):_
=XLOOKUP($G28, ItemsFinal[Fruit], ItemsFinal[Price]) is a #N/A error.  Please explain why this error occurred and how to fix it.


_Prompt (a teaching example on some aspect of Excel):_

Explain the Excel XLOOKUP function with a few examples.

A follow-up question could be: Should I use the XLOOKUP or VLOOKUP function in my Excel spreadsheet?


_Prompt:_


