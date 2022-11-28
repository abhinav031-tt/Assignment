Questions:

Q1.Count the number of Salesperson whose name begin with 'a/A'.

->select count(*) as number_of_Salesperson from SalesPeople where Sname LIKE 'a%';
+-----------------------+
| number_of_Salesperson |
+-----------------------+
|                     1 |
+-----------------------+


Q2.Display all the Salesperson whose all orders worth is more than Rs. 2000.

->select * from Salespeople inner join Orders ON Salespeople.Snum=Orders.Snum where Orders.Amt>2000;
+------+--------+---------+------+------+---------+------------+------+------+
| Snum | Sname  | City    | Comm | Onum | Amt     | Odate      | Cnum | Snum |
+------+--------+---------+------+------+---------+------------+------+------+
| 1001 | Peel   | London  |   12 | 3008 | 4273.00 | 1990-10-05 | 2006 | 1001 |
| 1001 | Peel   | London  |   12 | 3011 | 9891.88 | 1990-10-06 | 2006 | 1001 |
| 1002 | Serres | Sanjose |   13 | 3005 | 5160.45 | 1990-10-03 | 2003 | 1002 |
+------+--------+---------+------+------+---------+------------+------+------+


Q3.Count the number of Salesperson belonging to Newyork.

->select count(*) as number_of_Salesperson_belonging_to_Newyork from SalesPeople where City="Newyork";
+--------------------------------------------+
| number_of_Salesperson_belonging_to_Newyork |
+--------------------------------------------+
|                                          1 |
+--------------------------------------------+


Q4.Display the number of Salespeople belonging to London and belonging to Paris

select count(*) as number_of_Salesperson_belonging_to_London_And_Paris,City from SalesPeople
->where City='London' OR City='Paris';
+-----------------------------------------------------+--------+
| number_of_Salesperson_belonging_to_London_And_Paris | City   |
+-----------------------------------------------------+--------+
|                                                   2 | London |
+-----------------------------------------------------+--------+


Q5.Display the number of orders taken by each Salesperson and their date of orders.

select count(*) AS number_of_orders,Salespeople.Sname,orders.odate from Salespeople
->inner join Orders ON Salespeople.Snum=Orders.Snum Group by Salespeople.Sname Order by number_of_orders;
+------------------+---------+------------+
| number_of_orders | Sname   | odate      |
+------------------+---------+------------+
|                1 | Axelrod | 1990-10-04 |
|                1 | Motika  | 1990-10-03 |
|                2 | Rifkin  | 1990-10-03 |
|                3 | Peel    | 1990-10-03 |
|                3 | Serres  | 1990-10-03 |
+------------------+---------+------------+
