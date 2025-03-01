# BD-1
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
