# nosql-challenge

## Background

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. We've been contracted by the editors of a food magazine, *Eat Safe, Love*, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up

Using the `NoSQL_setup_starter.ipynb`, import the data provided in the `establishments.json` file.  Create a databased called `uk_foods` and the collection `establishments`.  Create an instance of the Mongo Client.

Confirm that you created the database and loaded the data properly:

- List the databases in MongoDB.
- Confirm that `uk_food` is listed.
- List the collection(s) in the database to ensure that `establishments` is there.
- Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.
- Assign the `establishments` collection to a variable to prepare the collection for use.

## Part 2: Update the Database

The magazine editors have some requested modifications for the database before we can perform any queries or analysis for them. Using the `NoSQL_setup_starter.ipynb` notebook, we will make the following changes to the `establishments` collection:

1. Add a new restaurant that just opened in Greenwich, but hasn't been rated yet.

2. Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.

3. Update the new restaurant with the `BusinessTypeID` we found.

4. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

5. Some of the number values are stored as strings, when they should be stored as numbers.

   - Use `update_many` to convert `latitude` and `longitude` to decimal numbers.
   - Use u`pdate_many` to convert `RatingValue` to integer numbers.

## Exploratory Analysis

*Eat Safe, Love* has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

Use NoSQL_analysis_starter.ipynb for this section of the challenge.

For each question:

- Use `count_documents` to display the number of documents contained in the result.

- Display the first document in the results using `pprint`.

- Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

Explore the database by answering the following questions

1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

## Folders and Files

1. **[`NoSQL_setup_starter.ipynb`](https://github.com/blmccourt/nosql-challenge/blob/main/NoSQL_setup_starter.ipynb)**

- Jupyter notebook with the scripts for *Part 1: Database and Jupyter Notebook Set Up* and *Part 2: Update the Database*.

2. **[`NoSQL_analysis_starter.ipynb`](https://github.com/blmccourt/nosql-challenge/blob/main/NoSQL_analysis_starter.ipynb)**

- Jupyter notebook with the scripts for *Part 3: Exploratory Analysis*.

3. **[Resources](https://github.com/blmccourt/nosql-challenge/tree/main/Resources)**

- Folder with the provided `json` file: `establishments.json`.
