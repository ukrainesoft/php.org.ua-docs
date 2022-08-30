Функції PostgreSQL

-   [« Базовое использование](pgsql.examples-queries.html)
    
-   [пгaffectedrows »](function.pg-affected-rows.html)
    
-   [PHP Manual](index.md)
    
-   [PostgreSQL](book.pgsql.md)
    
-   Функції PostgreSQL
    

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

-   [пгaffectedrows](function.pg-affected-rows.html) — Повертає кількість порушених запитом записів (кортежів)
-   [пгcancelquery](function.pg-cancel-query.html) - Зупинення асинхронного запиту.
-   [пгclientencoding](function.pg-client-encoding.html) - Отримання кодування клієнта.
-   [пгclose](function.pg-close.html) — Закриває з'єднання з базою даних PostgreSQL
-   [пгconnectpoll](function.pg-connect-poll.html) — Опитати статус спроби асинхронного з'єднання PostgreSQL.
-   [пгconnect](function.pg-connect.html) — Відкриває з'єднання з базою даних PostgreSQL
-   [пгconnectionbusy](function.pg-connection-busy.html) — Перевіряє, чи зайняте з'єднання зараз.
-   [пгconnectionreset](function.pg-connection-reset.html) - Скидання підключення (перепідключення)
-   [пгconnectionstatus](function.pg-connection-status.html) - Визначає стан підключення
-   [пгconsumeinput](function.pg-consume-input.html) — Читає вступні дані на з'єднанні
-   [пгconvert](function.pg-convert.html) — Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
-   [пгcopyfrom](function.pg-copy-from.html) — Вставляє записи з масиву до таблиці
-   [пгcopyто](function.pg-copy-to.html) — Копіює дані з таблиці до масиву
-   [пгdbname](function.pg-dbname.html) - Визначає ім'я бази даних
-   [пгdelete](function.pg-delete.html) - Видаляє записи
-   [пгendcopy](function.pg-end-copy.html) — Синхронізує з бекендом PostgreSQL
-   [пгescapebytea](function.pg-escape-bytea.html) — Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [пгescapeidentifier](function.pg-escape-identifier.html) — Екранує ідентифікатор для вставлення текстового поля
-   [пгescapeliteral](function.pg-escape-literal.html) — Екранувати літерал під час вставки у текстове поле
-   [пгescapestring](function.pg-escape-string.html) — Екранування спецсимволів у рядку запиту
-   [пгexecute](function.pg-execute.html) — Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат
-   [пгfetchallcolumns](function.pg-fetch-all-columns.html) — Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив
-   [пгfetchall](function.pg-fetch-all.html) — Вибирає всі дані з результату запиту та поміщає їх у масив
-   [пгfetcharray](function.pg-fetch-array.html) — Повертає рядок результату у вигляді масиву
-   [пгfetchassoc](function.pg-fetch-assoc.html) — Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [пгfetchobject](function.pg-fetch-object.html) — Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult](function.pg-fetch-result.html) — Повертає запис із результату запиту
-   [пгfetchrow](function.pg-fetch-row.html) — Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfieldісnull](function.pg-field-is-null.html) - Перевірка поля на значення SQL NULL
-   [пгfieldname](function.pg-field-name.html) - Повертає найменування поля
-   [пгfieldnum](function.pg-field-num.html) - Повертає порядковий номер іменованого поля
-   [пгfieldprtlen](function.pg-field-prtlen.html) — Повертає кількість символів, що друкуються.
-   [пгfieldsize](function.pg-field-size.html) — Повертає розмір поля
-   [пгfieldtable](function.pg-field-table.html) — Повертає назву або ідентифікатор таблиці, що містить задане поле
-   [пгfieldtypeoid](function.pg-field-type-oid.html) - Повертає ідентифікатор типу заданого поля
-   [пгfieldtype](function.pg-field-type.html) - Повертає ім'я типу заданого поля
-   [пгflush](function.pg-flush.html) — Скинути дані вихідного запиту на з'єднанні
-   [пгfreeresult](function.pg-free-result.html) — Очищення результату запиту та звільнення пам'яті
-   [пгgetnotify](function.pg-get-notify.html) — Отримання SQL NOTIFY повідомлення
-   [пгgetpid](function.pg-get-pid.html) — Отримує ID процесу сервера БД
-   [пгgetresult](function.pg-get-result.html) — Отримання результату асинхронного запиту
-   [пгhost](function.pg-host.html) — Повертає ім'я хоста, що відповідає підключенню
-   [пгinsert](function.pg-insert.html) — Заносить дані з масиву до таблиці баз даних
-   [пгlasterror](function.pg-last-error.html) — Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [пгlastnotice](function.pg-last-notice.html) — Повертає останнє повідомлення від сервера PostgreSQL
-   [пгlastoid](function.pg-last-oid.html) — Повертає OID останньому доданому до бази рядка
-   [пглоclose](function.pg-lo-close.html) - Закриває великий об'єкт
-   [пглоcreate](function.pg-lo-create.html) - Створює великий об'єкт
-   [пглоexport](function.pg-lo-export.html) — Виведення великого об'єкта у файл
-   [пглоimport](function.pg-lo-import.html) - Імпорт великого об'єкта з файлу
-   [пглоopen](function.pg-lo-open.html) — Відкриває великий об'єкт бази даних
-   [пглоreadall](function.pg-lo-read-all.html) — Читає вміст великого об'єкта та посилає безпосередньо до браузера
-   [пглоread](function.pg-lo-read.html) — Читає дані великого об'єкту
-   [пглоseek](function.pg-lo-seek.html) — Переміщує внутрішній покажчик великого об'єкту
-   [пглоtell](function.pg-lo-tell.html) — Повертає поточне положення внутрішнього покажчика великого об'єкту
-   [пглоtruncate](function.pg-lo-truncate.html) - Обрізає великий об'єкт
-   [пглоunlink](function.pg-lo-unlink.html) — Видалення великого об'єкту
-   [пглоwrite](function.pg-lo-write.html) — Записує дані у великий об'єкт
-   [пгmetadata](function.pg-meta-data.html) — Отримання метаданих таблиці
-   [пгnumfields](function.pg-num-fields.html) — Повертає кількість полів у вибірці
-   [пгnumrows](function.pg-num-rows.html) — Повертає кількість рядків у вибірці
-   [пгoptions](function.pg-options.html) — Отримання параметрів з'єднання із сервером баз даних
-   [пгparameterstatus](function.pg-parameter-status.html) — Перегляд поточних параметрів сервера
-   [пгpconnect](function.pg-pconnect.html) — Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгping](function.pg-ping.html) — Перевірка з'єднання з базою даних
-   [пгport](function.pg-port.html) — Повертає номер порту, який відповідає заданому з'єднанню
-   [пгprepare](function.pg-prepare.html) — Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [пгputline](function.pg-put-line.html) — Передає на PostgreSQL сервер рядок із завершальним нулем
-   [пгqueryparams](function.pg-query-params.html) — Надсилає параметризований запит на сервер, параметри передаються окремо від тексту запиту SQL
-   [пгquery](function.pg-query.html) — Виконує запит
-   [пгresulterrorfield](function.pg-result-error-field.html) — Повертає конкретне поле зі звіту про помилки
-   [пгresulterror](function.pg-result-error.html) — Повертає повідомлення про помилку, пов'язане із запитом результату
-   [пгresultseek](function.pg-result-seek.html) — Зміщує вказівник на рядок вибірки в екземплярі результату запиту
-   [пгresultstatus](function.pg-result-status.html) - Повертає стан результату запиту
-   [пгselect](function.pg-select.html) - Вибирає записи з бази даних
-   [пгsendexecute](function.pg-send-execute.html) - Запускає попередньо підготовлений SQL-запит та передає йому параметри; не чекає результату, що повертається
-   [пгsendprepare](function.pg-send-prepare.html) — Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [пгsendqueryparams](function.pg-send-query-params.html) — Надсилає параметризований запит на сервер, не чекає результату, що повертається.
-   [пгsendquery](function.pg-send-query.html) — Надсилає асинхронний запит
-   [пгsetclientencoding](function.pg-set-client-encoding.html) - Встановлює клієнтське кодування
-   [пгseterrorverbosity](function.pg-set-error-verbosity.html) — Визначає обсяг тексту повідомлень, що повертаються функціями pglasterror та pgresulterror
-   [пгsocket](function.pg-socket.html) — Отримати дескриптор тільки для читання на сокет, що лежить в основі з'єднання PostgreSQL
-   [пгtrace](function.pg-trace.html) — Включає трасування підключення PostgreSQL
-   [пгtransactionstatus](function.pg-transaction-status.html) — Повертає поточний стан транзакції на сервері
-   [пгtty](function.pg-tty.html) — Повертає ім'я терміналу TTY, пов'язане зі з'єднанням
-   [пгunescapebytea](function.pg-unescape-bytea.html) — Забирає екранування двійкових даних типу bytea
-   [пгuntrace](function.pg-untrace.html) — Вимикає трасування з'єднання з PostgreSQL
-   [пгupdate](function.pg-update.html) — Оновлення даних у таблиці
-   [пгversion](function.pg-version.html) — Повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера (якщо є)