---
navigation:
  - mysqlinfo.api.choosing.md: « Вибір API
  - mysqlinfo.concepts.md: Основні поняття "
  - index.md: PHP Manual
  - mysql.md: Огляд PHP драйверів MySQL
title: Вибір бібліотеки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вибір бібліотеки

Модулі mysqli та PDO\_MySQL - лише легковажні обгортки над бібліотеками написаними мовою C. Ці модулі можуть використовувати бібліотеки [mysqlnd](book.mysqlnd.md)и`libmysqlclient`. Вибір бібліотеки потрібно зробити на етапі компіляції.

Бібліотека mysqlnd є частиною дистрибутива PHP. Вона надає такі можливості як ліниве з'єднання (lazy connections) та кешування запитів. У бібліотеці libmysqlclient ці можливості недоступні. Тому вкрай рекомендується використовувати саме вбудовану бібліотеку mysqlnd. Для додаткової інформації дивіться [документацію mysqlnd](book.mysqlnd.md)

**Приклад #1 Команди конфігурування для mysqlnd та libmysqlclient**

//Рекомендована, компілює з mysqlnd $ ./configure --with-mysqli=mysqlnd --with-pdo-mysql=mysqlnd

//Рекомендована, компілює з mysqlnd $ ./configure --with-mysqli --with-pdo-mysql

//Не рекомендована, компілює з libmysqlclient $ ./configure --with-mysqli=/path/to/mysql\_config --with-pdo-mysql=/path/to/mysql\_config

**Порівняння можливостей бібліотек**

Рекомендується використовувати бібліотеку [mysqlnd](book.mysqlnd.md), а не MySQL Client Server library (libmysqlclient). Обидві бібліотеки розвиваються та підтримуються виробниками.

|  | MySQL native driver ([mysqlnd](book.mysqlnd.md)) | MySQL client server library (`libmysqlclient`) |
| --- | --- | --- |
| Частина дистрибутива PHP | Так | Ні |
| З'явилася у версії PHP | 5.3.0 | Немає даних |
| Ліцензія | PHP License 3.01 | Подвійна ліцензія |
| Статус розробки | Активний | Активний |
| Життєвий цикл | Закінчення не анонсовано | Закінчення не анонсовано |
| Компілювання за промовчанням (для всіх модулів MySQL) | Так | Ні |
| Підтримка протоколу стиснення | Так | Так |
| Підтримка SSL | Так | Так |
| Підтримка іменованих конвеєрів (named pipes) | Так | Так |
| Неблокуючі, асинхронні запити | Так | Ні |
| Статистика продуктивності | Так | Ні |
| LOAD LOCAL INFILE поважає директиву [open\_basedir](ini.core.md#ini.open-basedir) | Так | ні |
| Використовує штатний менеджер пам'яті PHP (тобто обмеження пам'яті PHP) | Так | Ні |
| Повертає числові значення як значення з плаваючою точкою (float) (COM\_QUERY) | Так | ні |
| Повертає числові значення як рядки (string) (COM\_QUERY) | Так | Так |
| Підтримка плагінів | Так | Обмежено |
| Автоматичне перепідключення | ні | опціонально |
