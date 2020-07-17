# __BA 510 Final Project__
### Bridget Weill

__1. Analyze & Understand the Data:__
   - Fairfield University Course Data from Fall 2014 to Spring 2019 seperated by Term and year. 
   - Within each term and year there were 2 CSVs, 'course_meetings.csv' & 'courses.csv'
   - Course catalogs for 2017-2018 and 2018-2019 are also provided as CSV's, 'CourseCatalog2017_2018.csv' & 'CourseCatalog2018_2019.csv'
    
__2. Normalized Relational Database:__

[Data Dictionary](CourseDataDictionary.md)
      
[ERD](CourseDataERD.pdf)
      
   - I began by organizing the data into an ERD & creating a data dictionary.
   - The data dictionary defines each column found in the tables of our ERD (which will become the terms in the dataset).
   
__3. SQLite database:__

   [Course Data ETL](CourseDataETL.ipynb)
  
   - Before creating the tables, I first created a database for the data, 'CourseData.db'
   - Next, I created our 7 tables, labeled the feature within each table along with their datatype and defined the primary keys.
   
__4. Data Extraction:__

   [Course Data ETL](CourseDataETL.ipynb)
   
   - I imported the data from each CSV into the 'CourseData.db' database.
   - To do this, I had to define the terms, define the filepath, read in the CSVs, and connect this data to SQL
   - To be sure the data was imported and imported correctly, I did a COUNT of the values from these 3 datafiles before moving on to the next step. 
   
   
__5. Populate Tables:__

   [Course Data ETL](CourseDataETL.ipynb)
   
   - With the data now put into the CourseData.db, I now filled the tables with the data. 
   - I inserted the data into the tables using the feature names in the CSVs to define which data went to each column.
   
__6. Integrity Check & Empty Tables:

   [Data Integrity](CourseDataTests.ipynb)
   
   - Finally, I checked out data for integrity and emptied the imported tables to clear up space.
   
__7. Data Warehouse__

   [Data Warehouse ERD](Class-Fact-Table.pdf)

   - Through a star schema, I began to build a data warehouse.
   - I first formulated questions I wanted to answer from the data, and then built the data warehouse around these questions.
   - The final Data Warehouse was put into and ERD

__8. Data Warehouse__

   [Data Warehouse](CourseDataWarehouseTest.ipynb)

   - By following along with the previous steps I took to build the CourseData tables, I filled the Data Warehouse ERD tables with data.
   - I created tables and used the data from the previously populated tables to fill these new tables.
   - Once again, I checked the data for integrity
   
__9. Queries__

   [Data Warehouse Queries](CourseDataWarehouseDemo.ipynb)

   - To put the data warehouse to use, I made queries to answer the questions I based the creation of our data warehouse off of.  