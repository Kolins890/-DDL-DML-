Домашнее задание к занятию «Работа с данными (DDL/DML)» Николай Чернов

Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

<img width="1366" height="533" alt="image" src="https://github.com/user-attachments/assets/1e30d6fd-b93e-4c12-80ce-0b72e5c39381" />

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

<img width="1358" height="685" alt="image" src="https://github.com/user-attachments/assets/9c110c6b-4c23-4409-b01c-9c988c1f404b" />

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

<img width="1366" height="689" alt="image" src="https://github.com/user-attachments/assets/8cb96d17-aab1-4459-be9d-435961683515" />

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

Задание 2

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id
actor	            actor_id
actor_info	      (составной ключ/нет явного PK)
address	          address_id
category	        category_id
city	            city_id
country	          country_id
customer	        customer_id
customer_list	    (представление, нет PK)
film	            film_id
film_actor	      (составной ключ: film_id, actor_id)
film_category	    (составной ключ: film_id, category_id)
film_list	        (представление, нет PK)
film_text	         film_id
inventory	         inventory_id
language	         language_id
payment	           payment_id
rental	           rental_id
sales_by_film_category	(представление, нет PK)
sales_by_store	    (представление, нет PK)
staff	             staff_id
staff_list	       (представление, нет PK)
store	             store_id
