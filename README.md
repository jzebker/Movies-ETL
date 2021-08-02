# Movies-ETL
## Overview
Help Britta create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables.

In particular:

Deliverable 1: Write an ETL Function to Read Three Data Files

Deliverable 2: Extract and Transform the Wikipedia Data

Deliverable 3: Extract and Transform the Kaggle data

Deliverable 4: Create the Movie Database

## Deliverable 1
[Notebook](https://github.com/jzebker/Movies-ETL/blob/main/ETL_function_test.ipynb)

• reads in "wikipedia-movies.json", "movies_metadata.csv", and "ratings.csv" files and converts to Pandas DataFrame (wiki_movies_df, kaggle_metadata, and ratings respectively)

<p align="center">
  <img width="851" alt="etlfunc" src="https://user-images.githubusercontent.com/84994321/127931822-7d6ddcde-28b3-40a1-8a29-bdd33431507d.png">
</p>

• output for "wikipedia-movies.json" as wiki_movies_df is within the linked notebook ("ETL_function_test.ipynb")

<p align="center">
  <img width="379" alt="wikioutput" src="https://user-images.githubusercontent.com/84994321/127931751-9c96ab97-d4a6-4e8e-a87a-60ff4de70bac.png">
</p>

• output for "movies_metadata.csv"" as kaggle_metadata is within the linked notebook ("ETL_function_test.ipynb")

<p align="center">
  <img width="399" alt="kaggleoutput" src="https://user-images.githubusercontent.com/84994321/127931700-aec30bac-8c32-4a55-bff7-d42f3784bd47.png">
</p>

• output for "ratings.csv" as ratings is within the linked notebook ("ETL_function_test.ipynb")

<p align="center">
  <img width="350" alt="ratingsoutput" src="https://user-images.githubusercontent.com/84994321/127931795-be7e9729-eed5-4452-95a4-a3a5c259b83c.png">
</p>

## Deliverable 2
[Notebook](https://github.com/jzebker/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb)
