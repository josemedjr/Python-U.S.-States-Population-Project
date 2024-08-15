## Web Scraping and Data Analysis on U.S. States Population using Python

## Problem Description
I utilized Beautiful Soup and web scraping techniques in Python to extract population data of U.S. states from different decades from Wikipedia. After collecting the data, I employed Pandas to structure it into a table and carried out data cleaning to improve its usability. With the cleaned data, I conducted a thorough analysis and developed visualizations to identify patterns in the population changes of U.S. states over different decades, with a focus on regional trends.


## Web Scraping and Data Cleaning
I started by importing BeautifulSoup and accessing the target website by retrieving the URL. Using the find_all function, I located the specific table on the webpage and stored it in a variable called "table." I then used find_all again to access the table headers (th), rows (tr), and individual data cells (td). With the data in hand, I imported Pandas to organize the titles and data into a structured table.

Next, I began the data cleaning process by dropping columns that were not relevant to my analysis, such as those labeled "#." I also renamed certain columns to ensure clarity, changing names like "State/Territory" and "Region" to more appropriate titles. Additionally, I standardized the entries in the "Region" column, replacing abbreviations like "NEng" with "New England." To maintain data integrity, I removed any duplicate rows and dropped unwanted rows by eliminating their indexes. Finally, I reset the index to ensure proper row numbering and saved the cleaned table as a CSV file for further use.

## Data Analysis
I began analyzing the data by first loading the CSV file into a DataFrame. To ensure that the columns were in the correct format, I used df.info() to check the data types of each column. For columns that needed to be converted to floats, I first removed any non-numerical characters, such as commas, by using str.replace(',', '').astype(float) for each relevant column. After this, I grouped the data by different regions of the country and created a new table. By transposing this table, I was able to visualize the changes in population over time. Additionally, I used a box plot and the describe() function to examine statistical values for each decade’s population data. Finally, I employed various visualizations, including bar charts, line graphs, and pie charts, to evaluate population changes in each region.











