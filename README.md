# Movies-ETL Documented assumptions
---

The approach I took was to create 1 main ETL function that would take in 3 arguments: a json file and 2 csv files. Then I aggregated all previously done steps into the main function, only leaving the cleanup function for json file outside the main function. 

Key assumptions:

-I used try and except in one place, for the most critical column - the imdb_id -- to account for any errors; I used (e) to get the exact error back in case if any errors.
-Assuming that columns are the same so I didn't use the try/except for column renaming, but if we were to reuse the function on a different version of the file it would be helpful to have try/except at the stage of column renaming
- Similar logic concerning columns to keep. Assuming 90% is a requirement that is still satisfactory with current and future versions of the file. Perhaps, in future we would need to drop this down to 70% for a more concentrated analysis but for now it's 90%.

I checked my code runs and populates the SQL table.


