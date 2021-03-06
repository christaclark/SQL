# SQL
Code and Slides for SQL Bootcamp @ General Assembly

What is a database?
  - An organized collection of data 
  - Organized overall by a schema (blueprint for db)
  - Organized into tables with different sets of data 
  - If each family is a set of data, a house would be the table, and the neighborhood would be the schema
  - Think many Excel sheets, but without so many limits
  
Why use a database?
  - Has a nice structures language, only need to know syntax
  - Access large amounts of data relatively quickly - Google SQL server??
  - Reliable and scalable
  - Many are ACID compliant - sensures your transactions are safely processed or that you're notified otherwise

Relational vs NoSQL
 - Relationtional: our database is built out of tables that talk to and relate to each other, needs schema
 - NoSQL: set up to help understand unstructured data, as there is no defined data structure (such ad MongoDB) using           JSON, popular with startups who don't know what the data will be, or what schema/ tables to build

SQL - Standes for Structured Query Language
  - Used to ask questions from the Database

Many different functions // What are we learning?
  - Create data storage
  - Add data
  - Transform  data
  - Aggregate data
  - Delete data

Data types // You need to get it in the correct format to be able to analyze:
  - Boolean or tiny INT  (0 or 1) : denotes whether a row is active using binary (like data expands in html)
  - INT - integer is any whole number
  - FLOAT (<n>,<m>) - number with "n" digits before the decimal and "m" digits after the decimal, you don't have to      limit numbers infront of the demcinal to allow huge numbers to be collected
  - DATETIME, TIMESTAMP, and DATE - various date and time combinations
  - CHAR(<length>) - text with a fixed length 
  - VARCHAR(<length>) - text with a given maximum length 
     - useful for building a schema and converting data once it's been pulled out (such as exporting to excel)

 ETL (Extract, Transform and Load):
  - How do we get all data to go into the same place/ server? Take Data from a 3rd party
  - MySQL -> commands -> file path 
  - You have to create a table with data types before you load the data into the table 
  - Make sure you define everything before running ETL!! - Python is the best languae for running it

Example: 
DROP TABLE IF EXISTS user_logs;
CREATE TABLE user_logs (
	event_id INT NOT NULL AUTO_INCREMENT, /* You can't have more than one Event_ID. */
	time_stamp TIMESTAMP NOT NULL,
	user_id INT NOT NULL,
	user_logged_in BOOLEAN,
	resolution_id INT,
	duration_on_page FLOAT(6,2),
	PRIMARY KEY (event_id)
);
