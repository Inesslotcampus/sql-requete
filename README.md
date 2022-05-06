## supprimer 1 article:

DELETE FROM `customers` 
WHERE `customers`.`id` = 3;


## ajouter un produit:

INSERT INTO `products` (`category_id`, `price`, `quantity`)

 VALUES ( '1','50', '2'); 

## Augmenter 5 % d'une catégorie:

UPDATE    products

SET       price = '(@price /100) * 5 + @price'

WHERE category_id =1


## Ajouter 100 à la quantité en stock d‘un produit:

UPDATE `products`

 SET `quantity` = '100'
 
 WHERE `products`.`id` = 15; 



## supprimer 1 article:

DELETE FROM `products` 
WHERE `products`.`id` = 6 » 

## supprimer les clients qui n'ont pas de commande :

DELETE A 
FROM customers AS A 
LEFT OUTER JOIN orders AS B ON B.customer_id = A.id 
WHERE B.customer_id is null; 

//la commande LEFT JOIN (aussi appelée LEFT OUTER JOIN) est un type de jointure entre 2 tables. Cela permet de lister tous les résultats de la table de gauche (left = gauche) même s’il n’y a pas de correspondance dans la deuxième tables.




## ajouter une commande à 3 produits
INSERT INTO orders (number, customer_id, date) VALUES ('0000000006', 3, NOW());

INSERT INTO order_product VALUES (6, 4, 1);

INSERT INTO order_product VALUES (6, 2, 1);

INSERT INTO order_product VALUES (6, 3, 1);
