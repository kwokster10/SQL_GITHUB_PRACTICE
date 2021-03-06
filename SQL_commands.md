# SQL_GITHUB_PRACTICE

## Creating a table called receipts with those columns
```
CREATE TABLE receipts (id INTEGER PRIMARY KEY AUTOINCREMENT, store TEXT, item TEXT, number_of_items NUMERIC, price NUMERIC, buy_date TEXT);
```

## Seed Data
```INSERT INTO receipts (store, item, number_of_items, price, buy_date) VALUES```
```
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
  ```

## All the attributes from all the receipts
```SELECT * FROM receipts;```
```
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
```

## The store and item names from all the receipts
```SELECT store, item FROM receipts;```
```
Sears|PS4
Toys R Us|XBox One
Toys R Us|TMNT Collectors Set
Sears|Lego Set
Strand|Blood Meridian
Strand|Ham on Rye
Community Books|The Last Tycoon
Macy's|Button Down Shirt
JC Penny|Nikes
JC Penny|tube socks
JC Penny|Reeboks
JC Penny|Umbrella, Red
JC Penny|Boxer Shorts
JC Penny|TMNT bedspread
Sears|Packers Jersey
Toys R Us|Life
Sears|laptop bag
```

## All the attributes from all purchases made at Toys R Us
```SELECT * FROM receipts WHERE store = "Toys R Us";```
```
2|Toys R Us|XBox One|1|500|January 21 2014
3|Toys R Us|TMNT Collectors Set|1|25|January 21 2014
16|Toys R Us|Life|1|25|March 24 2014
```

## The item name of each purchase made at Strand
```SELECT item FROM receipts WHERE store = "Strand";```
```
Blood Meridian
Ham on Rye
```

## The total number of items Peter purchased
```SELECT sum(number_of_items) FROM receipts;```
49

## The total number of items purchased at Sears
```SELECT sum(number_of_items) FROM receipts WHERE store = "Sears";```
27

## All the attributes of receipts where Peter bought multiple items
```SELECT * FROM receipts WHERE number_of_items > 1;```
```
5|Strand|Blood Meridian|3|12|March 21 2014
6|Strand|Ham on Rye|2|12|March 21 2014
8|Macy's|Button Down Shirt|3|28.5|March 22 2014
10|JC Penny|tube socks|3|28|March 23 2014
13|JC Penny|Boxer Shorts|3|20.75|March 23 2014
17|Sears|laptop bag|24|40.5|March 24 2014
```

## The average number of items purchased on a trip to JC Penny
```SELECT AVG(number_of_items) FROM receipts WHERE store = "JC Penny";```
1.66666666666667

## Add a new receipt representing the purchase of a single "Heatstreet Maple Bourbon", purchased for $40.99 at "Schnapps Haus" on the most recent fourth of July.
```INSERT INTO receipts (store, item, number_of_items, price, buy_date) VALUES("Schnapps Haus", "Heatstreet Maple Bourbon", 1, 40.99, "July 4 2014");```

-if I log it now: 

```SELECT * FROM receipts```
```
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
18|Schnapps Haus|Heatstreet Maple Bourbon|1|40.99|July 4 2014
```
-Yay! It added.


