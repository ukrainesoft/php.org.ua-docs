---
navigation:
  - pgsql.examples-queries.md: « Базовое использование
  - function.pg-affected-rows.md: пгaffectedrows »
  - index.md: PHP Manual
  - book.pgsql.md: PostgreSQL
title: Функції PostgreSQL
---
# Функції PostgreSQL

## Примітки

> **Зауваження**
> 
> Не всі функції можуть підтримуватись у зібраному модулі. Це залежить від версії вашої libpq (клієнтська бібліотека PostgreSQL) і як libpq була зібрана. Якщо модуль PostgreSQL для PHP відсутній, це означає, що версія вашої libpq не підтримується.

> **Зауваження**
> 
> Більшість функцій PostgreSQL приймають `connection` як перший необов'язковий параметр. Якщо параметр відсутній, використовується останнє відкрите з'єднання. Якщо такого не існує, то функція повертає **`false`**

> **Зауваження**
> 
> PostgreSQL автоматично переводить усі ідентифікатори (такі як імена таблиць/стовпців) у нижній регістр під час створення об'єкта та виконання запиту. Щоб змусити використовувати ідентифікатори в обох або тільки у верхньому регістрах, ви повинні екранувати ідентифікатор за допомогою подвійних лапок ("").

> **Зауваження**
> 
> У PostgreSQL немає спеціальних команд отримання інформації про схему БД (наприклад, всіх таблиць обраної бази даних). Але натомість у версіях PostgreSQL 7.4 і вище існує стандартна схема, яка називається `information_schema`. Вона містить системні уявлення (view) з усією необхідною інформацією легкодоступної формі. Для додаткової інформації дивіться [» документацию PostgreSQL](http://www.postgresql.org/docs/current/interactive/)

## Зміст

-   [пгaffectedrows](function.pg-affected-rows.md) — Повертає кількість порушених запитом записів (кортежів)
-   [пгcancelquery](function.pg-cancel-query.md) - Зупинення асинхронного запиту.
-   [пгclientencoding](function.pg-client-encoding.md) - Отримання кодування клієнта.
-   [пгclose](function.pg-close.md) — Закриває з'єднання з базою даних PostgreSQL
-   [пгconnectpoll](function.pg-connect-poll.md) — Опитати статус спроби асинхронного з'єднання PostgreSQL.
-   [пгconnect](function.pg-connect.md) — Відкриває з'єднання з базою даних PostgreSQL
-   [пгconnectionbusy](function.pg-connection-busy.md) — Перевіряє, чи зайняте з'єднання зараз.
-   [пгconnectionreset](function.pg-connection-reset.md) - Скидання підключення (перепідключення)
-   [пгconnectionstatus](function.pg-connection-status.md) - Визначає стан підключення
-   [пгconsumeinput](function.pg-consume-input.md) — Читає вступні дані на з'єднанні
-   [пгconvert](function.pg-convert.md) — Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
-   [пгcopyfrom](function.pg-copy-from.md) — Вставляє записи з масиву до таблиці
-   [пгcopyто](function.pg-copy-to.md) — Копіює дані з таблиці до масиву
-   [пгdbname](function.pg-dbname.md) - Визначає ім'я бази даних
-   [пгdelete](function.pg-delete.md) - Видаляє записи
-   [пгendcopy](function.pg-end-copy.md) — Синхронізує з бекендом PostgreSQL
-   [пгescapebytea](function.pg-escape-bytea.md) — Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [пгescapeidentifier](function.pg-escape-identifier.md) — Екранує ідентифікатор для вставлення текстового поля
-   [пгescapeliteral](function.pg-escape-literal.md) — Екранувати літерал під час вставки у текстове поле
-   [пгescapestring](function.pg-escape-string.md) — Екранування спецсимволів у рядку запиту
-   [пгexecute](function.pg-execute.md) — Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат
-   [пгfetchallcolumns](function.pg-fetch-all-columns.md) — Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив
-   [пгfetchall](function.pg-fetch-all.md) — Вибирає всі дані з результату запиту та поміщає їх у масив
-   [пгfetcharray](function.pg-fetch-array.md) — Повертає рядок результату у вигляді масиву
-   [пгfetchassoc](function.pg-fetch-assoc.md) — Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [пгfetchobject](function.pg-fetch-object.md) — Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult](function.pg-fetch-result.md) — Повертає запис із результату запиту
-   [пгfetchrow](function.pg-fetch-row.md) — Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfieldісnull](function.pg-field-is-null.md) - Перевірка поля на значення SQL NULL
-   [пгfieldname](function.pg-field-name.md) - Повертає найменування поля
-   [пгfieldnum](function.pg-field-num.md) - Повертає порядковий номер іменованого поля
-   [пгfieldprtlen](function.pg-field-prtlen.md) — Повертає кількість символів, що друкуються.
-   [пгfieldsize](function.pg-field-size.md) — Повертає розмір поля
-   [пгfieldtable](function.pg-field-table.md) — Повертає назву або ідентифікатор таблиці, що містить задане поле
-   [пгfieldtypeoid](function.pg-field-type-oid.md) - Повертає ідентифікатор типу заданого поля
-   [пгfieldtype](function.pg-field-type.md) - Повертає ім'я типу заданого поля
-   [пгflush](function.pg-flush.md) — Скинути дані вихідного запиту на з'єднанні
-   [пгfreeresult](function.pg-free-result.md) — Очищення результату запиту та звільнення пам'яті
-   [пгgetnotify](function.pg-get-notify.md) — Отримання SQL NOTIFY повідомлення
-   [пгgetpid](function.pg-get-pid.md) — Отримує ID процесу сервера БД
-   [пгgetresult](function.pg-get-result.md) — Отримання результату асинхронного запиту
-   [пгhost](function.pg-host.md) — Повертає ім'я хоста, що відповідає підключенню
-   [пгinsert](function.pg-insert.md) — Заносить дані з масиву до таблиці баз даних
-   [пгlasterror](function.pg-last-error.md) — Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [пгlastnotice](function.pg-last-notice.md) — Повертає останнє повідомлення від сервера PostgreSQL
-   [пгlastoid](function.pg-last-oid.md) — Повертає OID останньому доданому до бази рядка
-   [пглоclose](function.pg-lo-close.md) - Закриває великий об'єкт
-   [пглоcreate](function.pg-lo-create.md) - Створює великий об'єкт
-   [пглоexport](function.pg-lo-export.md) — Виведення великого об'єкта у файл
-   [пглоimport](function.pg-lo-import.md) - Імпорт великого об'єкта з файлу
-   [пглоopen](function.pg-lo-open.md) — Відкриває великий об'єкт бази даних
-   [пглоreadall](function.pg-lo-read-all.md) — Читає вміст великого об'єкта та посилає безпосередньо до браузера
-   [пглоread](function.pg-lo-read.md) — Читає дані великого об'єкту
-   [пглоseek](function.pg-lo-seek.md) — Переміщує внутрішній покажчик великого об'єкту
-   [пглоtell](function.pg-lo-tell.md) — Повертає поточне положення внутрішнього покажчика великого об'єкту
-   [пглоtruncate](function.pg-lo-truncate.md) - Обрізає великий об'єкт
-   [пглоunlink](function.pg-lo-unlink.md) — Видалення великого об'єкту
-   [пглоwrite](function.pg-lo-write.md) — Записує дані у великий об'єкт
-   [пгmetadata](function.pg-meta-data.md) — Отримання метаданих таблиці
-   [пгnumfields](function.pg-num-fields.md) — Повертає кількість полів у вибірці
-   [пгnumrows](function.pg-num-rows.md) — Повертає кількість рядків у вибірці
-   [пгoptions](function.pg-options.md) — Отримання параметрів з'єднання із сервером баз даних
-   [пгparameterstatus](function.pg-parameter-status.md) — Перегляд поточних параметрів сервера
-   [пгpconnect](function.pg-pconnect.md) — Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгping](function.pg-ping.md) — Перевірка з'єднання з базою даних
-   [пгport](function.pg-port.md) — Повертає номер порту, який відповідає заданому з'єднанню
-   [пгprepare](function.pg-prepare.md) — Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [пгputline](function.pg-put-line.md) — Передає на PostgreSQL сервер рядок із завершальним нулем
-   [пгqueryparams](function.pg-query-params.md) — Надсилає параметризований запит на сервер, параметри передаються окремо від тексту запиту SQL
-   [пгquery](function.pg-query.md) — Виконує запит
-   [пгresulterrorfield](function.pg-result-error-field.md) — Повертає конкретне поле зі звіту про помилки
-   [пгresulterror](function.pg-result-error.md) — Повертає повідомлення про помилку, пов'язане із запитом результату
-   [пгresultseek](function.pg-result-seek.md) — Зміщує вказівник на рядок вибірки в екземплярі результату запиту
-   [пгresultstatus](function.pg-result-status.md) - Повертає стан результату запиту
-   [пгselect](function.pg-select.md) - Вибирає записи з бази даних
-   [пгsendexecute](function.pg-send-execute.md) - Запускає попередньо підготовлений SQL-запит та передає йому параметри; не чекає результату, що повертається
-   [пгsendprepare](function.pg-send-prepare.md) — Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [пгsendqueryparams](function.pg-send-query-params.md) — Надсилає параметризований запит на сервер, не чекає результату, що повертається.
-   [пгsendquery](function.pg-send-query.md) — Надсилає асинхронний запит
-   [пгsetclientencoding](function.pg-set-client-encoding.md) - Встановлює клієнтське кодування
-   [пгseterrorverbosity](function.pg-set-error-verbosity.md) — Визначає обсяг тексту повідомлень, що повертаються функціями pglasterror та pgresulterror
-   [пгsocket](function.pg-socket.md) — Отримати дескриптор тільки для читання на сокет, що лежить в основі з'єднання PostgreSQL
-   [пгtrace](function.pg-trace.md) — Включає трасування підключення PostgreSQL
-   [пгtransactionstatus](function.pg-transaction-status.md) — Повертає поточний стан транзакції на сервері
-   [пгtty](function.pg-tty.md) — Повертає ім'я терміналу TTY, пов'язане зі з'єднанням
-   [пгunescapebytea](function.pg-unescape-bytea.md) — Забирає екранування двійкових даних типу bytea
-   [пгuntrace](function.pg-untrace.md) — Вимикає трасування з'єднання з PostgreSQL
-   [пгupdate](function.pg-update.md) — Оновлення даних у таблиці
-   [пгversion](function.pg-version.md) — Повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера (якщо є)
