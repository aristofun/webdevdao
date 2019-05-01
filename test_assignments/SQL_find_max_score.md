## SQL: запрос к БД 

Есть таблица `users` [ id (int), email (str), score (int), company_id(int) ]  со связью «один ко многим» с таблицей `companies` [ id(int), name(str) ]  

**Задание**

Получить выборку [ id, email, score, company_id ] с максимальным `score` по каждой компании.

[Users]     

| ID      | email           | score      | company_id |
|  ------- | --------------- | ---------- | ---------- |
| 1       | user1@test.home | 8          | 1          |
| 2       | user2@test.home | 8          | 2          |
| 3       | user3@test.home | 4          | 1          |
| 4       | user4@test.home | 1          | 2          |
| 5       | user5@test.home | 2          | 1          |
| 6       | user6@test.home | 3          | 2          |
| 7       | user7@test.home | 0          | 1          |
| 8       | user8@test.home | 6          | 2          |
| 9       | user9@test.home | 9          | 1          |


[Result]     

| ID      | email           | score      | company_id |
|  ------- | --------------- | ---------- | ---------- |
| 9       | user9@test.home | 9          | 1          |
| 2       | user2@test.home | 8          | 2          |