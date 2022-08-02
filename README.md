# Movies-ETL
# ETL Process
## Purpose of the Project Movies-ETL
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs assistance to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. this project will refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

## Deliverable 1: Write an ETL Function to Read Three Data Files 

In this Deliverable we are going to do ETL process, code refactoring and write a function that reads the 3 data files and creates the data frames.
The code for this deliverable part is :

[ETL_function_test.ipynb](https://github.com/urvish7/Movies-ETL/blob/main/ETL_function_test.ipynb)


The output of the 3 data frames are :

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/wiki_movies-df.png)

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/Kaggle_metadata.png)

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/rating.png)

## Deliverable 2: Extract and Transform the Wikipedia Data

In this deliverable we are going to do ETL process and code refactoring. We are going to extract and transform the wikipedia data so merge can be done with Kaggle
metadata. Also, extracting the IMDB IDs using a regular expression string and dropping duplicates we are going to use the try-expect block to catch the errors. 

[ETL_clean_wiki_movies.ipynb](https://github.com/urvish7/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb)


the dataframes that are created in this deliverable are: 

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/dev2_wiki_movies.png)

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/dev2_wiki_movies_tolist.png)


## Deliverable 3: Extract and Transform the Kaggle Data

In this deliverable we are going to use the pandas, ETL process and code refactoring. we will extract and transform the Kaggle metadata and MovieLens rating data then convert the transformed data into separate dataframes. It will merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, merging the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

[ETL_clean_kaggle_data.ipynb](https://github.com/urvish7/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb)


The dataframes associated with this task are:

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/dev3_movies.png)

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/dev3_movies_with_ratings.png)

![](https://github.com/urvish7/Movies-ETL/blob/main/ScreenShots/dev3_wiki_movies.png)


## Deliverable 4: Create the Movie Database

In this deliverable we are going to use the ETL process, Pandas, code refactoring and PostgreSQL to add the movies_df dataframe and MovieLens rating CSV data to the SQL database.


[ETL_create_database.ipynb](https://github.com/urvish7/Movies-ETL/blob/main/ETL_create_database.ipynb)


## The output in the database for the row counts:

### Movies Query :

![](https://github.com/urvish7/Movies-ETL/blob/main/Resources/movies_query.png)


### Ratings Query:
![](https://github.com/urvish7/Movies-ETL/blob/main/Resources/ratings_query.png)


Note: The movies_metadata.csv in the Resources folder is in compressed mode please download if you like to view it.
