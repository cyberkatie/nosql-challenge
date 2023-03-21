# nosql-challenge
Penn Data Science Bootcamp Module 12 Assignment

# Part 1: Database and Jupyter Notebook Set Up
* Used NoSQL_setup_starter.ipynb for this section of the challenge.
* Imported the data provided in the establishments.json file from the Terminal. Named the database uk_food and the collection establishments. Copied the text used to import data from the Terminal to a markdown cell in the notebook.
* Within the notebook, the needed libraries were imported: PyMongo and Pretty Print (pprint).
* Created an instance of the Mongo Client.
* Confirmed that the database was created and loaded the data properly:
  * Listed the databases that exist in MongoDB. Confirmed that uk_food is listed.
  * Listed the collection(s) in the database to ensure that establishments is there.
  * Found and displayed one document in the establishments collection using find_one and displayed with pprint.
  * Assigned the establishments collection to a variable to prepare the collection for use.
  
# Part 2: Update the Database
* Added a new restaurant to the database
* Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields.
* Updated the new restaurant with the BusinessTypeID that was found.
* We are not interested in any establishments in Dover, so checked how many documents contain the Dover Local Authority. Then, removed any establishments within the Dover Local Authority from the database, and checked the number of documents to ensure they were deleted.
* Used update_many to convert latitude and longitude to decimal numbers.

# Part 3: Exploratory Analysis

* For each question:
  * Used count_documents to display the number of documents contained in the result.
  * Displayed the first document in the results using pprint.
  * Converted the result to a Pandas DataFrame, printed the number of rows in the DataFrame, and displayed the first 10 rows.

* Which establishments have a hygiene score equal to 20?
* Which establishments in London have a RatingValue greater than or equal to 4?
*What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
