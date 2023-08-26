# Analyze 911 (Emergency) Calls Data

## Tools : Python

## Library : Numpy, Pandas, Seaborn, Matplotlib

# Task

1. import the file and check the info().
2. Find out the top 5 zipcodes for 911 calls.
3. Chcek the top 5 townships (twp) for 911 calls.
4. Take a look at the 'title' column, how many unique title codes are there.
5. Creating New feature. I have specified "Reasons/Departments" from the title code. These are EMS, Fire, and Traffic. I have Used 
   .apply() with a custom lambda expression to create a new column called "Reason" that contains this string value.
6. What is the most common Reason for a 911 call based off of this new column?
7. I have used seaborn to create a countplot of 911 calls by Reason.
8. what is the data type of the objects in the timeStamp column?
9. I have checked is timestamps are still strings?
10. I have used Jupyter's tab method to explore the various attributes which anyone can call. Now that the timestamp column are actually 
   DateTime objects, used .apply() to create 3 new columns called Hour, Month, and Day of Week. Create these columns based off of the 
   timeStamp column.
11. How the Day of Week is an integer 0-6. That time I have used the .map() with this dictionary to map the actual string names to the 
    day of the week: **
    dmap = {0:'Mon',1:'Tue',2:'Wed',3:'Thu',4:'Fri',5:'Sat',6:'Sun'}
12. I have used seaborn to create a countplot of the Day of Week column with the hue based off of the Reason column.
13. DOing the same process for Month.
14. Some months are missing in this Plot?
15. So, I create a gropuby object called byMonth, wheregroup the DataFrame by the month column and use the count() method for 
    aggregation. Then used the head() method on this returned DataFrame.
16. I create a simple plot off of the dataframe indicating the count of calls per month.
17. I have used seaborn's lmplot() to create a linear fit on the number of calls per month and reset the index to a column.
18. Create a new column called 'Date' that contains the date from the timeStamp column and used .date() method.
19. Then I have done groupby with the Date column with the count() aggregate and create a plot of counts of 911 calls.
20.  Again recreate this plot but create 3 separate plots with each plot representing a Reason for the 911 call.
21. Finally create heatmaps with seaborn and calls data. First I restructure the dataframe so that the columns become the Hours and the 
    Index becomes the Day of the Week and for this purpose use unstack method beacuse it convert data to matrix form. 
22. Then create a HeatMap using this new DataFrame.
23. Again, create a clustermap using this DataFrame
24. Now, repeat the same plots and operations, for a DataFrame that shows the Month as the column.
25. Once create the same Heatmap and also Clustermap using new Month dataframe.
