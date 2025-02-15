# BD-1
1) select * from orders
 
![image](https://github.com/user-attachments/assets/c159b8d4-57e7-48c6-bb68-48ab2cb4c71e)

2) Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
 
select * from orders where status in('cancelled', 'in_progress', 'delivery')

![image](https://github.com/user-attachments/assets/53a5a7e3-3640-455a-a8cb-8cd26f51e20e)

3) Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
 
select * from orders where status in('cancelled', 'new')

![image](https://github.com/user-attachments/assets/bfab63b2-a81c-4355-b4c9-c7d8cdf9cb40)

4) Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.
 
select id,sum from orders where products_count > 3

![image](https://github.com/user-attachments/assets/0c4166f1-2ee3-40c3-a71b-b95cb6044392)
