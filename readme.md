1.	How many users? 50 SELECT COUNT(*) FROM users;

2.	5 most expensive items: SELECT *  FROM items ORDER BY price DESC LIMIT 5 ;
	25|Small Cotton Gloves|Automotive, Shoes & Beauty|Multi-layered modular 		service-desk|9984
	83|Small Wooden Computer|Health|Re-engineered fault-tolerant adapter|9859
	100|Awesome Granite Pants|Toys & Books|Upgradable 24/7 access|9790
	40|Sleek Wooden Hat|Music & Baby|Quality-focused heuristic info-mediaries|		9390
	60|Ergonomic Steel Car|Books & Outdoors|Enterprise-wide secondary firmware|		9341
3.	Fantastic Steel Chair(book only) Awesome Granite Pants (contains book)
4.	Corrine Little SELECT users.first_name, users.last_name, addresses.street  		FROM users INNER JOIN addresses WHERE users.id = addresses.user_id AND 		addresses.street = '6439 Zetta Hills';
5.	SELECT users.id FROM users WHERE users.first_name = 'Virginie'; Gets ID 
	
	UPDATE addresses SET city = 'New York' ,zip = '10108' WHERE user_id = 39 AND 	city = 'Roxanehaven' ;
6.	SELECT SUM(price) FROM items WHERE category LIKE '%tools%' , SELECT 			SUM(price) FROM items WHERE category LIKE 'tools';
7.	SELECT SUM(quantity) FROM orders; 2125
8.	SELECT orders.quantity, items.category, items.price, SUM(items.price* 		orders.quantity)  FROM orders INNER JOIN items WHERE orders.item_id = 		items.id AND items.category LIKE '%books%';
	quantity|category|price|SUM(items.price* orders.quantity)
9.	INSERT INTO orders VALUES (null, 51 ,15,6,datetime());

ADVENTURE 
1.	SELECT SUM(orders.quantity), items.title, items.price, SUM(items.price * orders.quantity)  FROM orders INNER JOIN items WHERE orders.item_id = items.id GROUP BY items.title ORDER BY SUM(orders.quantity) DESC; <---ordered most
Ordered most 72|Rustic Steel Shirt|615|30464 AND 72|Incredible Granite Car|7295|525240
SELECT SUM(orders.quantity), items.title, items.price, SUM(items.price * orders.quantity)  FROM orders INNER JOIN items WHERE orders.item_id = items.id GROUP BY items.title ORDER BY SUM(orders.quantity * items.price) DESC; <---highest grossing

