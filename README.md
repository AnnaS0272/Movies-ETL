# Movies-ETL Documented assumptions
---

The approach I took was to create 1 main ETL function that would take in 3 arguments: a json file and 2 csv files. Then I aggregated all previously done steps into the main function, only leaving the cleanup function for json file outside the main function. I used try and except in one place, for the most critical column - the imdb_id -- to account for any errors; I used (e) to get the exact error back in case if any errors.

I checked my code runs and populates the SQL table.


