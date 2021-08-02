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

• filters out TV shows

<p align="center">
  <img width="574" alt="tvfilter" src="https://user-images.githubusercontent.com/84994321/127932857-3c741b49-aa4f-4ccf-b97c-6e9bd36ab740.png">
</p>

• extracts IMDb ID from imdb_link with regex, includes try-except block for error handling

<p align="center">
  <img width="1046" alt="imdbidtryexcept" src="https://user-images.githubusercontent.com/84994321/127932959-080df79c-1e2e-4e67-be63-3f277211d6cf.png">
</p>

• removes columns with >90% null values, then converts box_office values to string and matches 2 different forms with regex

<p align="center">
  <img width="1176" alt="nonnullregexboxoffice" src="https://user-images.githubusercontent.com/84994321/127933239-24fea834-af79-4c1d-82f7-a48a07490d35.png">
</p>

• cleans ***box office*** and ***budget*** columns using the "parse_dollars" function and ***release date*** and ***running time*** columns with regex date forms and time forms respectively

<p align="center">
  <img width="1186" alt="cleancolumnsparsedollars" src="https://user-images.githubusercontent.com/84994321/127933716-22609fc5-391d-4c86-affc-5774a5b2fd60.png">
</p>

• wiki_movies output is in the notebook linked above for Deliverable 2

<sup><ital>Note</ital> - superfluous release date and budget columns have been dropped</sup>

<p align="center">
  <img width="583" alt="wiki_movies_dfoutput" src="https://user-images.githubusercontent.com/84994321/127933856-1c09b41b-7097-43ac-9265-81edb2f25a53.png"><img width="587" alt="wiki_movies_dfcolumns" src="https://user-images.githubusercontent.com/84994321/127933837-1bf5f848-6a2f-4340-bb18-0b09c9329b95.png">
</p>

## Deliverable 3
[Notebook](https://github.com/jzebker/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb)

• extracts and transforms the kaggle data and the ratings data

• cleans kaggle data

<p align="center">
  <img width="920" alt="cleankaggle" src="https://user-images.githubusercontent.com/84994321/127934716-3c20c88e-732e-42d8-a3db-a15d30495aef.png">
</p>

• merges wiki and kaggle data

<p align="center">
  <img width="911" alt="mergedf" src="https://user-images.githubusercontent.com/84994321/127934760-19102b7f-5f72-47fd-b0a1-7ecfc1124aee.png">
</p>

• drops unnecessary columns and fills in missing data in merged DataFrame

<p align="center">
  <img width="1128" alt="dropandfillmissing" src="https://user-images.githubusercontent.com/84994321/127934864-8b74f29d-2d66-4423-858f-62cde1be2da2.png">
</p>

• filters merged DataFrame for specific columns and renames them appropriately

<p align="center">
  <img width="1178" alt="filterandrename" src="https://user-images.githubusercontent.com/84994321/127934916-b0d029df-ad32-4818-94a4-6b35ca28e27c.png">
</p>

