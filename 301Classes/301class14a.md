## DB Normalization

![Image](https://i.ytimg.com/vi/ABwD8IYByfk/maxresdefault.jpg)
*Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.* 
*Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:*

- Identify salespeople in your organization
- List all customers your company calls upon to sell a product
- Identify which salespeople call on specific customers.
![Image](https://www.essentialsql.com/wp-content/uploads/2014/06/FirstNormalFormUnormalized-1.png?ezimgfmt=ng:webp/ngcb3)

*By limiting a table to one purpose you reduce the number of duplicate data contained within your database. This eliminates some issues stemming from database modifications.*

*There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries.*

Duplicated information presents two problems:
- It increases storage and decrease performance.
- It becomes more difficult to maintain data changes.

here are three modification anomalies that can occur:
- Insert Anomaly
- Update Anomaly
- Deletion Anomaly

#### There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. 


- First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.

- Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.

- Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key

