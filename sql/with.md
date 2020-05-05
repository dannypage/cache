# WITH

Makes it much easier to represent sub-queries, or pre-process data before the main query. Also allows for iterative data exploration, as you can return the results, and then capture it in the WITH query before moving on to the final query.

```
WITH query_name1 AS (
     SELECT ...
     )
   , query_name2 AS (
     SELECT ...
       FROM query_name1
        ...
     )

SELECT ...
```

