# BD-1
                                    ЛАБА №1
1) select * from orders
 
![image](https://github.com/user-attachments/assets/3151874b-305d-4401-b9ca-49abbe8d75c7)

2) Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
 
select * from orders where status in('cancelled', 'in_progress', 'delivery')

![image](https://github.com/user-attachments/assets/ff7a0c52-ac09-4e25-af5e-802dc26cd986)

3) Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
 
select * from orders where status in('cancelled', 'new')

![image](https://github.com/user-attachments/assets/1640c8ea-9aab-4723-a759-12a5f5a3a910)

4) Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.
 
select id,sum from orders where products_count > 3

![image](https://github.com/user-attachments/assets/5c21e159-ca1d-4626-8593-f041aca3ab8b)

                                    ЛАБА №2
                                    
1) Выберите из таблицы orders 3 самых дешевых заказа за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте

![image](https://github.com/user-attachments/assets/a013a79a-1cd5-4b17-b3ac-1baaeaf58db9)

SELECT * FROM orders WHERE STATUS !='canseled' order by sum ASC LIMIT 3

2) Выберите из таблицы orders 2 самых дорогих заказов за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/e3eae9d3-7df4-45df-868b-d63c97d9ab93)

SELECT * FROM orders WHERE STATUS !='canseled' order by SUM desc LIMIT 2

3) Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

![image](https://github.com/user-attachments/assets/820709d5-6471-4737-b7a4-726b2341f6f1)

INSERT INTO orders (id, products, SUM) VALUES (6,4,8000)

4) Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

![image](https://github.com/user-attachments/assets/b379f091-6866-4797-8454-9ca9862cc8e5)

INSERT INTO products (id,NAME,count,price) VALUES (7,'VR-очки',2,70000)

5) В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

![image](https://github.com/user-attachments/assets/3d415960-8ad8-4914-a38b-0be22cd122c3)

UPDATE products SET NAME='PS5' WHERE NAME='IMAC'

                                    ЛАБА №3
                                    
 Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.

Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/8c40f261-e61a-438a-a779-ad3c5e21e3ea)

CREATE TABLE USERS (
    id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50)
);
INSERT INTO USERS (id,first_name,last_name) VALUES
(1, 'Дмитрий', 'Иванов'),
(2, 'Анатолий', 'Белый'),
(3, 'Денис','Давыдов');









