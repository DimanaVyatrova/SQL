# SQL

## Fundamental Syntax
### Comparison Operators
- not equal to `<>` or `!=`
- the others are the standard ones - `>`, `<`, `>=`, `<=`, `=`
They can be used not only on numerical data. When applied on string data, the comparison operators filter based on alphabetical order.
`month > ‘J’ `  - > selects only the months that start with “j” or later in the alphabet
### Arithmetic in SQL
Arithmetic can be performed with the operators +, -, *, /
However, it can only be performed across values in columns in the same row. If arithmetic operations need to be performed across multiple rows, aggregate functions must be used.
### Logical Operators
`LIKE` - used to match similar values rather than exact ones
use % as a wildcard to represent any character or a set of characters
use _ to substitute an individual character
`SELECT * FROM Movies WHERE name LIKE ‘Year%’`

`IN` - used to specify a list of values to be included in the results
WHERE year_rank IN (1, 2, 3)
WHERE artist IN (‘Madonna’, ‘Brithey’, ‘Beyonce’)
It is useful when used with a subquery: IN (SELECT ….)


BETWEEN
WHERE year_rank BETWEEN 5 AND 10
is the same as
WHERE year_rank >= 5 AND year_rank <= 10


IS NULL / IS NOT NULL - can be used to check if a value, for example in a WHERE clause, in null or not null
WHERE artist IS NULL
WHERE artist = NULL will not work


AND, OR, NOT - used in the standard way


ORDER BY - used to sort the result by one or more columns
SELECT * 
FROM Movies
WHERE year_rank <= 3
ORDER BY year DESC, year_rank
Instead of using the names of the columns, the numbers of the columns (the order they appear in) can be used too
