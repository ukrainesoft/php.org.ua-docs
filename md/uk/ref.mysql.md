---
navigation:
  - mysql.examples-basic.md: « Оглядовий приклад модуля MySQL
  - function.mysql-affected-rows.md: mysqlaffectedrows »
  - index.md: PHP Manual
  - book.mysql.md: MySQL (Original)
title: Функції СУБД MySQL
---
# Функції СУБД MySQL

## Примітки

> **Зауваження**
> 
> Більшість функцій MySQL приймають `link_identifier` як останній, опціональний параметр. Якщо він не вказаний, використовується останнє відкрите з'єднання. Якщо з'єднань немає, модуль намагається відкрити з'єднання використовуючи параметри, зазначені в php.ini. У разі невдачі функції повертають **`false`**. . **`false`**

## Зміст

-   [mysqlaffectedrows](function.mysql-affected-rows.md) — Повертає кількість порушених минулою операцією рядів
-   [mysqlclientencoding](function.mysql-client-encoding.md) — Повертає кодування з'єднання
-   [mysqlclose](function.mysql-close.md) — Закриває з'єднання із сервером MySQL
-   [mysqlconnect](function.mysql-connect.md) — Відкриває з'єднання із сервером MySQL
-   [mysqlcreateдб](function.mysql-create-db.md) - Створює базу даних MySQL
-   [mysqldataseek](function.mysql-data-seek.md) — Переміщує внутрішній покажчик у результаті запиту
-   [mysqlдбname](function.mysql-db-name.md) — Повертає назву бази даних із виклику до mysqllistdbs
-   [mysqlдбquery](function.mysql-db-query.md) — Перемикається на вказану базу даних та надсилає запит
-   [mysqldropдб](function.mysql-drop-db.md) — Знищує базу даних MySQL
-   [mysqlerrno](function.mysql-errno.md) — Повертає чисельний код помилки виконання останньої операції з MySQL
-   [mysqlerror](function.mysql-error.md) — Повертає текст помилки останньої операції з MySQL
-   [mysqlescapestring](function.mysql-escape-string.md) — Екранує рядок для використання у mysqlquery
-   [mysqlfetcharray](function.mysql-fetch-array.md) — Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysqlfetchassoc](function.mysql-fetch-assoc.md) — Повертає ряд результатів запиту як асоціативний масив.
-   [mysqlfetchfield](function.mysql-fetch-field.md) — Повертає інформацію про колонку з результату запиту як об'єкта
-   [mysqlfetchlengths](function.mysql-fetch-lengths.md) - Повертає довжину кожного поля в результаті
-   [mysqlfetchobject](function.mysql-fetch-object.md) — Обробляє ряд результатів запиту та повертає об'єкт
-   [mysqlfetchrow](function.mysql-fetch-row.md) — Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysqlfieldflags](function.mysql-field-flags.md) — Повертає прапори, пов'язані із зазначеним полем результату запиту
-   [mysqlfieldlen](function.mysql-field-len.md) — Повертає довжину вказаного поля
-   [mysqlfieldname](function.mysql-field-name.md) — Повертає назву вказаної колонки результату запиту
-   [mysqlfieldseek](function.mysql-field-seek.md) - Встановлює внутрішній покажчик результату на передане зміщення поля
-   [mysqlfieldtable](function.mysql-field-table.md) — Повертає назву таблиці, якій належить зазначене поле
-   [mysqlfieldtype](function.mysql-field-type.md) — Повертає тип вказаного поля із результату запиту
-   [mysqlfreeresult](function.mysql-free-result.md) - Звільняє пам'ять від результату запиту
-   [mysqlgetclientinfo](function.mysql-get-client-info.md) — Повертає дані про MySQL-клієнт
-   [mysqlgethostinfo](function.mysql-get-host-info.md) — Повертає інформацію про з'єднання з MySQL
-   [mysqlgetprotoinfo](function.mysql-get-proto-info.md) — Повертає інформацію про протокол MySQL
-   [mysqlgetserverinfo](function.mysql-get-server-info.md) — Повертає інформацію про сервер MySQL
-   [mysqlinfo](function.mysql-info.md) — Повертає інформацію про останній запит
-   [mysqlinsertід](function.mysql-insert-id.md) — Повертає ідентифікатор, згенерований за останнього INSERT-запиту
-   [mysqllistdbs](function.mysql-list-dbs.md) — Повертає список баз даних, доступних на сервері
-   [mysqllistfields](function.mysql-list-fields.md) — Повертає список колонок таблиці
-   [mysqllistprocesses](function.mysql-list-processes.md) - Повертає список процесів MySQL
-   [mysqllisttables](function.mysql-list-tables.md) - Повертає список таблиць бази даних MySQL
-   [mysqlnumfields](function.mysql-num-fields.md) — Повертає кількість полів результату запиту
-   [mysqlnumrows](function.mysql-num-rows.md) - Повертає кількість рядів результату запиту
-   [mysqlpconnect](function.mysql-pconnect.md) — Встановлює постійне з'єднання із сервером MySQL
-   [mysqlping](function.mysql-ping.md) — Перевіряє з'єднання з сервером та переєднується за потреби
-   [mysqlquery](function.mysql-query.md) — Надсилає запит MySQL
-   [mysqlrealescapestring](function.mysql-real-escape-string.md) — Екранує спеціальні символи у рядках для використання у виразах SQL
-   [mysqlresult](function.mysql-result.md) — Повертає дані результату запиту
-   [mysqlselectдб](function.mysql-select-db.md) - Вибирає базу даних MySQL
-   [mysqlsetcharset](function.mysql-set-charset.md) - Встановлює кодування клієнта
-   [mysqlstat](function.mysql-stat.md) — Повертає поточний статус сервера
-   [mysqltablename](function.mysql-tablename.md) — Повертає ім'я таблиці, яка містить вказане поле
-   [mysqlthreadід](function.mysql-thread-id.md) — Повертає ідентифікатор потоку.
-   [mysqlunbufferedquery](function.mysql-unbuffered-query.md) — Надсилає запит MySQL без авто-обробки результату та його буферизації
