# BigData-Assignment1

Introduction:
Our objective is to load the JHU CSSE COVID-19 Dataset using Spark/Hadoop and generate a monthly report of the top 10 states having the highest (Infection Fatality Ratio or Case Fatality Ratio).
Implementation:
In this implementation we used Spark to load the dataset and Plotly along with Pandas for plotting the data in a gaph.
Loading the Data:
•	Utilized the os module to access the file names from the dataset directory.
•	Segregated the files based on the year, organizing them for further processing.
•	Implemented a loop to read and load the CSV files using spark.read.csv.
•	Created separate DataFrames for each month by performing union operations on all files per month.
Processing the Data:
•	Utilized the segregated data to extract the Case_Fatality_Ratio from each DataFrame.
•	Calculated the average Case_Fatality_Ratio for each state over the month.
•	Conducted a none value omission to handle missing or undefined values in the data.
Monthly Report Generation (console output):
•	By taking the output from the Data Processing stage we perform a sort on that data and get the top 10 States.
•	Then print them to the console.
Graph Generation:
•	In order to generate the graph we make use of Pandas and Plotly packages.
•	As the state names are in a full form in the dataset we need to convert them to a shorter format that is acceptable by the Plotly inorder to generate the graph.
•	In the code convertDataToPlot function does this conversion to short format of State names.
•	Once it is done we pass the data to the PlotMap function that will cross verify the State names and then creates a graph in such a way that, when we hover over a state in the graph we see a overlay that will have the state, state_code, Infection_Fatality_Ratio details.
