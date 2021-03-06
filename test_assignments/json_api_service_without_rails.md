## Требуется создать JSON API сервис на Ruby без использования Ruby on Rails.

В качестве веб-фреймворка, необходимо использовать *sinatra, hanami, roda* или что-нибудь другое, но **не** *Ruby on Rails*. Доступ к БД можете осуществлять с помощью *ORM (active_record, sequel, rom)*, можете и без *ORM*, как посчитаете нужным.


**Сущности:**

1. User.
    - Имеет только логин.
2. Post.
    - Принадлежит юзеру.
    - Имеет заголовок, содержание, айпи автора (сохраняется отдельно для каждого поста).
3. Rating.
    - Принадлежит посту.
    - Принимает значение от 1 до 5.

**Экшены:**

1. Создать пост.
    - Принимает заголовок и содержание поста (не могут быть пустыми), а также логин и айпи автора. Если автора с таким логином еще нет, необходимо его создать.
    - Возвращает либо атрибуты поста со статусом 200, либо ошибки валидации со статусом 422.
2. Поставить оценку посту.
    - Принимает айди поста и значение.
    - Возвращает новый средний рейтинг поста.
    - **Важно:** *экшен должен корректно отрабатывать при любом количестве конкурентных запросов на оценку одного и того же поста.*
3. Получить топ N постов по среднему рейтингу.
    - Просто массив объектов с заголовками и содержанием.


4. Получить список айпи, с которых постило несколько разных авторов.
    - Массив объектов с полями: айпи и массив логинов авторов.

**Дополнительно:**

- Базу данных используем *PostgreSQL*. Для девелопмента написать скрипт в *db/seeds.rb*, который генерирует тестовые данные. Часть постов должна получить оценки. Скрипт должен использовать созданный *JSON API* сервер (можно посылать запросы курлом или еще чем-нибудь).
- Постов в базе должно быть хотя бы 200к, авторов лучше сделать в районе 100 штук, айпишников использовать штук 50 разных.
- Экшены должны на стандартном железе работать достаточно быстро как для указанного объема данных (быстрее 100 мс, если будет работать медленнее, то ничего страшного, все равно присылайте решение), так и для намного большего, то есть нужен хороший запас в плане оптимизации запросов. Для этого можно использовать денормализацию данных и любые другие средства БД. Можно использовать любые нужные гемы, обязательно наличие спеков, хорошо покрывающих разные кейсы. Архитектуру сервиса организуйте на "свой вкус". Желательно не использовать генераторов и вообще обойтись без лишних мусорных файлов в репозитории.
