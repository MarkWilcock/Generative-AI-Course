# Exercise - Analyse Supercars from the 1970s

MT Cars is a famous statistical dataset.  The data comes from the 1974 Motor Trend US magazine and contains fuel consumption and 10 aspects of automobile design and performance for 32  supercars of the time.  The objective of this exercise is to analyse what factors contribute to fuel efficiency (measured in the mpg column).

Download the data from [here](./Resources/mtcars.csv).

Here are some suggested prompts to start your analysis.  The first prompt describes of the columns – this is useful as the variable names are difficult to understand

*Initial Prompt*
Act as an data analyst.  The attached data has a details of 32 cars from the 1970s. Here is the description of the columns.
* model, Model Name
* mpg, Miles/(US) gallon
* cyl, Number of cylinders
* disp, Displacement (cu.in.)
* hp, Gross horsepower
* drat, Rear axle ratio
* wt, Weight (1000 lbs)
* qsec, 1/4 mile time
* vs, Engine (0 = V-shaped, 1 = straight)
* am, Transmission (0 = automatic, 1 = manual)
* gear, Number of forward gears
* carb, Number of carburettors

*Subsequent prompts*
* To make the charts more readable use Transmission rather than am and Automatic  / Manual labels for the values rather than 0 / 1
* Create similar scatter charts but use engine shape on the legend
* Is there a correlation between weight and horsepower?
* Add a column to the data indicating where each of these cars was manufactured: US, Europe or Asia.
* Analyse fuel efficiency by Origin _(in my practice run, the response to the previous prompt created a column named Origin)_
* Is it possible to buy any of these cars today?

<!--
FYI: This is data from the US and the 1970s so is expressed on American Imperial units.  The mpg is expressed in miles per US gallon and weight in pounds (lb).  You may want to convert to more familiar units such as miles per litre.  There are 3.785 litres in a US gallon.  A pounds (lb) of weight is 0.454 kg. 
-->
