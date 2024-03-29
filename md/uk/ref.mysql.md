---
navigation:
  - mysql.examples-basic.md: « Оглядовий приклад модуля MySQL
  - function.mysql-affected-rows.md: mysql\_affected\_rows »
  - index.md: PHP Manual
  - book.mysql.md: MySQL (Original)
title: Функції СУБД MySQL
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції СУБД MySQL

## Примітки

> **Зауваження** :
> 
> Більшість функцій MySQL приймають `link_identifier` як останній, опціональний параметр. Якщо він не вказаний, використовується останнє відкрите з'єднання. Якщо з'єднань немає, модуль намагається відкрити з'єднання використовуючи параметри, зазначені в php.ini. У разі невдачі функції повертають **`false`**. . **`false`**

## Зміст

-   [mysql\_affected\_rows](function.mysql-affected-rows.md)— Повертає кількість порушених минулою операцією рядів
-   [mysql\_client\_encoding](function.mysql-client-encoding.md)— Повертає кодування з'єднання
-   [mysql\_close](function.mysql-close.md)— Закриває з'єднання із сервером MySQL
-   [mysql\_connect](function.mysql-connect.md)— Відкриває з'єднання із сервером MySQL
-   [mysql\_create\_db](function.mysql-create-db.md) \- Створює базу даних MySQL
-   [mysql\_data\_seek](function.mysql-data-seek.md)— Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_db\_name](function.mysql-db-name.md)— Повертає назву бази даних із виклику до mysql\_list\_dbs
-   [mysql\_db\_query](function.mysql-db-query.md)— Перемикається на вказану базу даних та надсилає запит
-   [mysql\_drop\_db](function.mysql-drop-db.md)— Знищує базу даних MySQL
-   [mysql\_errno](function.mysql-errno.md)— Повертає чисельний код помилки виконання останньої операції з MySQL
-   [mysql\_error](function.mysql-error.md)— Повертає текст помилки останньої операції з MySQL
-   [mysql\_escape\_string](function.mysql-escape-string.md)— Екранує рядок для використання у mysql\_query
-   [mysql\_fetch\_array](function.mysql-fetch-array.md)— Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_assoc](function.mysql-fetch-assoc.md)— Повертає ряд результатів запиту як асоціативний масив.
-   [mysql\_fetch\_field](function.mysql-fetch-field.md)— Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysql\_fetch\_lengths](function.mysql-fetch-lengths.md) \- Повертає довжину кожного поля в результаті
-   [mysql\_fetch\_object](function.mysql-fetch-object.md)— Обробляє ряд результатів запиту та повертає об'єкт
-   [mysql\_fetch\_row](function.mysql-fetch-row.md)— Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_field\_flags](function.mysql-field-flags.md)— Повертає прапори, пов'язані із зазначеним полем результату запиту
-   [mysql\_field\_len](function.mysql-field-len.md)— Повертає довжину вказаного поля
-   [mysql\_field\_name](function.mysql-field-name.md)— Повертає назву вказаної колонки результату запиту
-   [mysql\_field\_seek](function.mysql-field-seek.md) \- Встановлює внутрішній покажчик результату на передане зміщення поля
-   [mysql\_field\_table](function.mysql-field-table.md)— Повертає назву таблиці, якій належить зазначене поле
-   [mysql\_field\_type](function.mysql-field-type.md)— Повертає тип вказаного поля із результату запиту
-   [mysql\_free\_result](function.mysql-free-result.md) \- Звільняє пам'ять від результату запиту
-   [mysql\_get\_client\_info](function.mysql-get-client-info.md)— Повертає дані про MySQL-клієнт
-   [mysql\_get\_host\_info](function.mysql-get-host-info.md)— Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_proto\_info](function.mysql-get-proto-info.md)— Повертає інформацію про протокол MySQL
-   [mysql\_get\_server\_info](function.mysql-get-server-info.md)— Повертає інформацію про сервер MySQL
-   [mysql\_info](function.mysql-info.md)— Повертає інформацію про останній запит
-   [mysql\_insert\_id](function.mysql-insert-id.md)— Повертає ідентифікатор, згенерований за останнього INSERT-запиту
-   [mysql\_list\_dbs](function.mysql-list-dbs.md)— Повертає список баз даних, доступних на сервері
-   [mysql\_list\_fields](function.mysql-list-fields.md)— Повертає список колонок таблиці
-   [mysql\_list\_processes](function.mysql-list-processes.md) \- Повертає список процесів MySQL
-   [mysql\_list\_tables](function.mysql-list-tables.md) \- Повертає список таблиць бази даних MySQL
-   [mysql\_num\_fields](function.mysql-num-fields.md)— Повертає кількість полів результату запиту
-   [mysql\_num\_rows](function.mysql-num-rows.md) \- Повертає кількість рядів результату запиту
-   [mysql\_pconnect](function.mysql-pconnect.md)— Встановлює постійне з'єднання із сервером MySQL
-   [mysql\_ping](function.mysql-ping.md)— Перевіряє з'єднання з сервером та переєднується за потреби
-   [mysql\_query](function.mysql-query.md)— Надсилає запит MySQL
-   [mysql\_real\_escape\_string](function.mysql-real-escape-string.md)— Екранує спеціальні символи у рядках для використання у виразах SQL
-   [mysql\_result](function.mysql-result.md)— Повертає дані результату запиту
-   [mysql\_select\_db](function.mysql-select-db.md) \- Вибирає базу даних MySQL
-   [mysql\_set\_charset](function.mysql-set-charset.md) \- Встановлює кодування клієнта
-   [mysql\_stat](function.mysql-stat.md)— Повертає поточний статус сервера
-   [mysql\_tablename](function.mysql-tablename.md)— Повертає ім'я таблиці, яка містить вказане поле
-   [mysql\_thread\_id](function.mysql-thread-id.md)— Повертає ідентифікатор потоку.
-   [mysql\_unbuffered\_query](function.mysql-unbuffered-query.md)— Надсилає запит MySQL без авто-обробки результату та його буферизації
