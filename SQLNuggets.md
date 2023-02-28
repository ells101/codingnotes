SQL Tips / Tricks / Things to Remember
========

- NoSQL = Non relational database (NOT-ONlY SQL) or SQL (Relational Database)
- Common SQL databases:
  - MySQL most popular open source SQL database.
  - Oracle also made by same company as MySQL but paid for. Lots of advantages over MySQL usually used by larger companies.
  - Postgres open-source for web-apps.
  - SQLite, well suited for bundling database with application.
  - MS SQL Server, not open source but very common in large enterprises. To interact with database there's loads of tools to pick from. AZURE or SQL Server management are popular.
- 1st, Second and Third normal forms are ways of normalising data.
- Comment with double dash i.e. "--"
- We can use DECIMAL like so: DECIMAL(4, 2) == (precision, scale). 4 digits, 2 numbers after the decimal point. (4,2) can store: 12.35
- FLOAT also stores decimals. FLOAT(n) where n is the max digits. More useful for very small or very big numbers. Not suitable for exact values.
- BIT takes value 1 or 0. (Represents TRUE or FALSE).
- Null does not equal null. Nothing equals null! Think of null as representing a missing value.
- Use Identity key word like so to add primary keys automatically: " likecourse_id INT PRIMARY KEY IDENTITY(1,1) ". (starting number, increment)
