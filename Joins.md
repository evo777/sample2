A join is a way in SQL to combine data from two or more tables. This will be used in a query that produces results from columns spanning many tables and compiles them.

![Visualizations](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/SQL_Joins.svg/2000px-SQL_Joins.svg.png)

## Types:
* INNER JOIN: produces results where there is a match from both tables.
* LEFT OUTER JOIN (LEFT JOIN): produces results where there is a match from the first (or left) table. If there is data from the second (right) table, it is included, but is not required for a successful query. Where data is missing from the right table, null is put in that cell of the results.
* RIGHT OUTER JOIN (RIGHT JOIN): produces results where there is a match from the second (or right) table. If there is data from the first (left) table, it is included, but it is not required for a successful query. Where data is missing from the left table, null is put in that cell of the results.
* FULL OUTER JOIN (OUTER JOIN): produces results equivalent to if one were to do a left and right outer join at the same time. Retrieves all of the results from both tables regardless of whether there is matching data in the other table. Similar to the other outer joins, missing data is filled in with null.
* CROSS JOIN: produces results that are every combination of the rows of the first and second table
* SELF JOIN: produces results that are from a table joined with itself as if the one table were two separate tables (e.g. SELECT a.column_name, b.column_name... FROM table1 a, table1 b WHERE a.common_field = b.common_field;)