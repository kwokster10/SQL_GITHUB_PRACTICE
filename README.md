# SQL_GITHUB_PRACTICE

## Creating a table called receipts with those columns
CREATE TABLE receipts (id INTEGER PRIMARY KEY AUTOINCREMENT, store TEXT, item TEXT, number_of_items NUMERIC, price NUMERIC, buy_date TEXT);

## Seed Data
INSERT INTO receipts (store, item, number_of_items, price, buy_date) VALUES
  ('Sears', 'PS4', 1, 400, 'January 21 2014'),
  ('Toys R Us', 'XBox One', 1, 500, 'January 21 2014'),
  ('Toys R Us', 'TMNT Collectors Set', 1, 25, 'January 21 2014'),
  ('Sears', 'Lego Set', 1, 40, 'January 21 2014'),
  ('Strand', 'Blood Meridian', 3, 12, 'March 21 2014'),
  ('Strand', 'Ham on Rye', 2, 12, 'March 21 2014'),
  ('Community Books', 'The Last Tycoon', 1, 14, 'March 21 2014'),
  ('Macy''s', 'Button Down Shirt', 3, 28.50, 'March 22 2014'),
  ('JC Penny', 'Nikes', 1, 100, 'March 23 2014'),
  ('JC Penny', 'tube socks', 3, 28, 'March 23 2014'),
  ('JC Penny', 'Reeboks', 1, 60, 'March 23 2014'),
  ('JC Penny', 'Umbrella, Red', 1, 10.50, 'March 23 2014'),
  ('JC Penny', 'Boxer Shorts', 3, 20.75, 'March 23 2014'),
  ('JC Penny', 'TMNT bedspread', 1, 20, 'March 23 2014'),
  ('Sears', 'Packers Jersey', 1, 50, 'March 24 2014'),
  ('Toys R Us', 'Life', 1, 25, 'March 24 2014'),
  ('Sears', 'laptop bag', 24, 40.50, 'March 24 2014');

 ## All the attributes from all the receipts
 sqlite> SELECT * FROM receipts;
1|Sears|PS4|1|400|January 21 2014
2|Toys R Us|XBox One|1|500|January 21 2014
3|Toys R Us|TMNT Collectors Set|1|25|January 21 2014
4|Sears|Lego Set|1|40|January 21 2014
5|Strand|Blood Meridian|3|12|March 21 2014
6|Strand|Ham on Rye|2|12|March 21 2014
7|Community Books|The Last Tycoon|1|14|March 21 2014
8|Macy's|Button Down Shirt|3|28.5|March 22 2014
9|JC Penny|Nikes|1|100|March 23 2014
10|JC Penny|tube socks|3|28|March 23 2014
11|JC Penny|Reeboks|1|60|March 23 2014
12|JC Penny|Umbrella, Red|1|10.5|March 23 2014
13|JC Penny|Boxer Shorts|3|20.75|March 23 2014
14|JC Penny|TMNT bedspread|1|20|March 23 2014
15|Sears|Packers Jersey|1|50|March 24 2014
16|Toys R Us|Life|1|25|March 24 2014
17|Sears|laptop bag|24|40.5|March 24 2014

// The store and item names from all the receipts


