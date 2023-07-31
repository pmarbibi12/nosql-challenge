# nosql-challenge
by Panfilo Marbibi  

# contents
- Resources (dir)
  - establishments.json
- NoSQL_analysis.ipynb
- NoSQL_setup.ipynb

# summary
- NoSQL_setup.ipynb
  - This jupyter notebook utilizes pyMongo to consstruct and edit a noSQL database.
  - imports data from establishments.json
  - creates the database 'uk_food'
  - creates the collection 'establishments'
  - enters a new entry called 'Penang Flavours'
  - assigns the proper BusinessTypeID to the Penang Flavours document by querying similar establishments that have the same BusinessType = 'Restaurant/Cafe/Canteen'
  - searches and excludes establishments/documents that are associated with the 'LocalAuthorityName': 'Dover' from the database
  - updates the latitude and longitude to the proper attribute type - double(float)
  - checks for non 1-5 rating values
  - removes any non 1-5 rating values and replaces them with None/Null
  - updates all instances of rating values to integer values
- NoSQL_analysis.ipynb
  - This jupyter notebook uses the database that was setup using NoSQL_setup.ipynb and performs several analysis on the database
  - find establishments that have a hygiene score of 20
  - creates a Pandas DataFrame with the found establishments
  - finds establishments in London have a 'RatingValue' greater than or equal to 4
  - creates a Pandass DataFrame from the above results and displays the number of rows in the data frame - 33 found
  - finds the top 5 establishments with a 'RatingValue' rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"
  - results are saved into a Pandas DataFrame
  - using a pipeline, queries establishments in each Local Authority area that have a hygiene score of 0 and returns the number of rows - 55 found
  - creates a Pandas DataFrame from the above results
  - shows the top 10 results
 
# disclaimer
code used in the jupyter notebooks are derived from classroom activities and discussions
