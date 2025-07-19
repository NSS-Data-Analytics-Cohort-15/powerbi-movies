## Power BI Movies Exercise
In this exercise, you'll be making use of Power BI to answer questions using multiple data sources.

First, import all 4 tables from the movie_casts database. 
Then, use the "Manage relationships" button to create the following relationships:
* best_actresses <-> people
* best_actors <-> people
* people <-> casts

Next, connect to your local movies database and import the 4 tables from it. You can do this by creating a PostgresSQL database connection and using localhost as the server. Once you have loaded the tables, create relationships with the movie_casts tables.

1. Have more actors or actresses won multiple awards?
2. Which actors have the most Oscar nominations without ever winning? What about actresses?
3. Make a scatterplot for length vs budget.  Then make each mpaa rating represented by a different color.
4. Who is the top actor or actress in terms of total profit? (Profit is worldwide gross minus budget.) Hint: You may want to add a New Quick Measure to the revenue table. 
5. Who is the top actor or actress in terms of total profit who has not been nominated for an Oscar? Hint: You may want to use the Transform Data button to make a table of actors or actresses who have never won an oscar. You can use an [Anti-Join](https://learn.microsoft.com/en-us/power-query/merge-queries-left-anti) to find people who don't appear in the best_actors or best_actresses table.
6. What is the average IMDB rating for all movies?  What about movies that have an actor with at least 1 award win?  What about movies that have an actress with at least 1 award win? Hint: Ensure that the cross-filters on the relationships between tables will allow you to filter ratings based on the awards tables.
7. How do the average IMDB ratings compare for movies that have either an actor or actress with an Oscar win to those that do not? Hint: Create a measure to find the total number of wins. Then make a column that checks whether this total is at least 1. 