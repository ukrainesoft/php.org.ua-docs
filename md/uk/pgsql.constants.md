Обумовлені константи

-   [« Типи ресурсів](pgsql.resources.html)
    
-   [Приклади »](pgsql.examples.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL](book.pgsql.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`PGSQL_LIBPQ_VERSION`** (string)

Коротке позначення версії libpq, що містить лише цифри та точки.

**`PGSQL_LIBPQ_VERSION_STR`** (string)

До PHP 8.0.0 – довге позначення версії libpq, яке включає інформацію про компілятор. Починаючи з PHP 8.0.0, значення ідентичне **`PGSQL_LIBPQ_VERSION`**, а використання **`PGSQL_LIBPQ_VERSION_STR`** застаріло.

**`PGSQL_ASSOC`** (int)

Передається у функцію [пгfetcharray()](function.pg-fetch-array.html). Повертає асоціативний масив 'ім'я поля' => 'значення поля'.

**`PGSQL_NUM`** (int)

Передається у функцію [пгfetcharray()](function.pg-fetch-array.html). Повертає нумерований масив 'номер поля' => 'значення поля'.

**`PGSQL_BOTH`** (int)

Передається у функцію [пгfetcharray()](function.pg-fetch-array.html). Повертає масив значень поля, нумерований (за номером поля) та асоціативний (на ім'я поля).

**`PGSQL_CONNECT_FORCE_NEW`** (int)

Передається у функцію [пгconnect()](function.pg-connect.html) для примусового створення нового з'єднання замість використання ідентичного існуючого.

**`PGSQL_CONNECT_ASYNC`** (int)

Передається в [пгconnect()](function.pg-connect.html) для створення асинхронного з'єднання.

**`PGSQL_CONNECTION_AUTH_OK`** (int)

**`PGSQL_CONNECTION_AWAITING_RESPONSE`** (int)

**`PGSQL_CONNECTION_BAD`** (int)

Повертається функцією [пгconnectionstatus()](function.pg-connection-status.html), вказує на непрацездатність з'єднання з базою даних

**`PGSQL_CONNECTION_MADE`** (int)

**`PGSQL_CONNECTION_OK`** (int)

Повертається функцією [пгconnectionstatus()](function.pg-connection-status.html), вказує на нормальний (робочий) стан з'єднання з базою даних

**`PGSQL_CONNECTION_SETENV`** (int)

**`PGSQL_CONNECTION_SSL_STARTUP`** (int)

**`PGSQL_CONNECTION_STARTED`** (int)

**`PGSQL_SEEK_SET`** (int)

Передається у функцію [пглоseek()](function.pg-lo-seek.html). Операція пошуку розпочне роботу з початку об'єкта.

**`PGSQL_SEEK_CUR`** (int)

Передається у функцію [пглоseek()](function.pg-lo-seek.html). Операція пошуку розпочне роботу з поточної позиції.

**`PGSQL_SEEK_END`** (int)

Передається у функцію [пглоseek()](function.pg-lo-seek.html). Операція пошуку розпочне роботу з кінця об'єкта.

**`PGSQL_EMPTY_QUERY`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Означає, що відправлений на сервер рядок був порожнім.

**`PGSQL_COMMAND_OK`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Означає успішне завершення команди, яка не повертає дані.

**`PGSQL_TUPLES_OK`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Означає успішне завершення команди, яка повертає будь-які дані (наприклад, `SELECT` або `SHOW`

**`PGSQL_COPY_OUT`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Повідомляє, що було розпочато копіювання даних із сервера.

**`PGSQL_COPY_IN`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Повідомляє, щоб розпочато копіювання даних на сервер.

**`PGSQL_BAD_RESPONSE`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Повідомляє, що відповідь від сервера не розпізнано.

**`PGSQL_NONFATAL_ERROR`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Повідомляє, що виникла некритична (повідомлення чи попередження) помилка.

**`PGSQL_FATAL_ERROR`** (int)

Повертається функцією [пгresultstatus()](function.pg-result-status.html). Повідомляє, що сталась критична помилка.

**`PGSQL_TRANSACTION_IDLE`** (int)

Повертається функцією [пгtransactionstatus()](function.pg-transaction-status.html). Означає, що з'єднання на даний момент не діє і не знаходиться в рамках транзакції.

**`PGSQL_TRANSACTION_ACTIVE`** (int)

Повертається функцією [пгtransactionstatus()](function.pg-transaction-status.html). Означає стан, коли команда перебуває у процесі виконання. Запит через з'єднання надіслано, але виконання ще не завершено.

**`PGSQL_TRANSACTION_INTRANS`** (int)

Повертається функцією [пгtransactionstatus()](function.pg-transaction-status.html). Це означає, що з'єднання простоює і знаходиться в рамках транзакції.

**`PGSQL_TRANSACTION_INERROR`** (int)

Повертається функцією [пгtransactionstatus()](function.pg-transaction-status.html). Означає, що з'єднання простоює і знаходиться в рамках транзакції потерпілої під час виконання.

**`PGSQL_TRANSACTION_UNKNOWN`** (int)

Повертається функцією [пгtransactionstatus()](function.pg-transaction-status.html). Означає, що з'єднання розірвано.

**`PGSQL_DIAG_SEVERITY`** (int)

Передається у функцію [пгresulterrorfield()](function.pg-result-error-field.html). Повідомляє про скруту. Можливі лише перелічені значення: `ERROR` `FATAL`, або `PANIC` (у повідомленні про помилку), або `WARNING` `NOTICE` `DEBUG` `INFO`, або `LOG` (у повідомленні), або переклад перерахованих значень відповідно до локалізації. Поле завжди визначене.

**`PGSQL_DIAG_SQLSTATE`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Код помилки SQLSTATE. Код SQLSTATE визначає тип помилки, що відбулася; він може бути використаний прикладною програмою при виконанні специфічних операцій (таких як обробка помилки) у відповідь на помилку бази даних. Це поле завжди визначено та його значення не залежить від локалізації.

**`PGSQL_DIAG_MESSAGE_PRIMARY`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Основне легкочитане повідомлення про помилку (зазвичай один рядок). Поле завжди визначене.

**`PGSQL_DIAG_MESSAGE_DETAIL`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Деталізація: додаткове повідомлення про помилку, що містить докладнішу інформацію про проблему. Може містити кілька рядків.

**`PGSQL_DIAG_MESSAGE_HINT`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Підказка: вказівка ​​на можливі шляхи усунення помилки. Відрізняється від деталізації помилки тим, що це просто пропозиції (можливо помилкові), а чи не точна інформація. Може містити кілька рядків.

**`PGSQL_DIAG_STATEMENT_POSITION`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Рядок, що містить десяткове ціле число, що вказує на позицію курсора у вихідному виразі, де сталася помилка. Перший символ має індекс 1, позиції обчислюються символами, а чи не в байтах.

**`PGSQL_DIAG_INTERNAL_POSITION`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Визначення також, що і для поля \*\*`PG_DIAG_STATEMENT_POSITION`\*\*але використовується у випадках, коли курсор вказує на команду, згенеровану сервером БД. У таких випадках завжди з'являється поле **`PG_DIAG_INTERNAL_QUERY`**

**`PGSQL_DIAG_INTERNAL_QUERY`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Текст помилки, згенерованої внутрішньою командою СУБД, у якій сталася помилка. Це може бути, наприклад, SQL-запит, сформований функцією PL/pgSQL.

**`PGSQL_DIAG_CONTEXT`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Вказівка ​​на контекст, де сталася помилка. В основному містить трасування запрограмованих функцій та автоматично згенерованих запитів. Трасування виводиться рядково, починаючи з останнього рядка.

**`PGSQL_DIAG_SOURCE_FILE`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Ім'я файлу вихідного коду PostgreSQL, у якому зазначено помилку.

**`PGSQL_DIAG_SOURCE_LINE`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Номер рядка файлу вихідного коду PostgreSQL, де зазначено помилку.

**`PGSQL_DIAG_SOURCE_FUNCTION`** (int)

Передається в [пгresulterrorfield()](function.pg-result-error-field.html). Ім'я функції у вихідному коді PostgreSQL, що повідомляє про помилку.

**`PGSQL_DIAG_SCHEMA_NAME`** (string)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_TABLE_NAME`** (string)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_COLUMN_NAME`** (string)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_DATATYPE_NAME`** (string)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_CONSTRAINT_NAME`** (string)

Додано до PHP 7.3.0.

**`PGSQL_ERRORS_TERSE`** (int)

Передається в [пгseterrorverbosity()](function.pg-set-error-verbosity.html). Дає припис, що повідомлення, що видаються, будуть містити тільки важливість помилки, основний текст і покажчик на місце, де вона відбулася; ця інформація зазвичай міститься в один рядок.

**`PGSQL_ERRORS_DEFAULT`** (int)

Передається в [пгseterrorverbosity()](function.pg-set-error-verbosity.html). У режимі за промовчанням повідомлення про помилки містять описану вище інформацію, а також деталізацію, підказку або поля з контекстом помилки (можуть займати кілька рядків).

**`PGSQL_ERRORS_VERBOSE`** (int)

Передається в [пгseterrorverbosity()](function.pg-set-error-verbosity.html). Задає режим, у якому у повідомлення будуть включені всі поля.

**`PGSQL_NOTICE_LAST`** (int)

Використовується [пгlastnotice()](function.pg-last-notice.html). Доступно з PHP 7.1.0.

**`PGSQL_NOTICE_ALL`** (int)

Використовується [пгlastnotice()](function.pg-last-notice.html). Доступно з PHP 7.1.0.

**`PGSQL_NOTICE_CLEAR`** (int)

Використовується [пгlastnotice()](function.pg-last-notice.html). Доступно з PHP 7.1.0.

**`PGSQL_STATUS_LONG`** (int)

Передається в [пгresultstatus()](function.pg-result-status.html). Вказує на те, що як значення, що повертається, очікується числовий код.

**`PGSQL_STATUS_STRING`** (int)

Передається в [пгresultstatus()](function.pg-result-status.html). Вказує на те, що як значення, що повертається, очікується текстове подання статусу.

**`PGSQL_CONV_IGNORE_DEFAULT`** (int)

Передається в [пгconvert()](function.pg-convert.html). Ігнорувати значення за замовчуванням у таблиці у процесі перетворення.

**`PGSQL_CONV_FORCE_NULL`** (int)

Передається в [пгconvert()](function.pg-convert.html). Замінювати порожні рядки string на SQL `NULL` при перетворенні.

**`PGSQL_CONV_IGNORE_NOT_NULL`** (int)

Передається в [пгconvert()](function.pg-convert.html). Вказує, що не потрібно конвертувати **`null`** у стовпці SQL `NOT NULL`

**`PGSQL_DML_NO_CONV`** (int)

Передається в [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.html). Усі параметри передаються у вихідному вигляді. Ручне екранування обов'язково, якщо параметри містять дані користувача. Використовуйте для цього [пгescapestring()](function.pg-escape-string.html)

**`PGSQL_DML_EXEC`** (int)

Передається в [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.html). Виконати запит за допомогою цих опцій.

**`PGSQL_DML_ASYNC`** (int)

Передається в [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.html). Виконайте асинхронний запит за допомогою цих функцій.

**`PGSQL_DML_STRING`** (int)

Передається в [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.html). Повернути рядок із виконаним запитом.

**`PGSQL_DML_ESCAPE`** (int)

Передається в [пгinsert()](function.pg-insert.html) [пгselect()](function.pg-select.html) [пгupdate()](function.pg-update.html) і [пгdelete()](function.pg-delete.html). Застосувати екранування до всіх параметрів замість внутрішнього виклику [пгconvert()](function.pg-convert.html). Ця опція пропускає перегляд метаданих. Запит може бути таким самим швидким, як і [пгquery()](function.pg-query.html) і [пгsendquery()](function.pg-send-query.html)

**`PGSQL_POLLING_FAILED`** (int)

Повертається функцією [пгconnectpoll()](function.pg-connect-poll.html) і свідчить про те, що спроба з'єднання провалилася.

**`PGSQL_POLLING_READING`** (int)

Повертається функцією [пгconnectpoll()](function.pg-connect-poll.html) і вказує на те, що з'єднання очікує, коли сокет PostgreSQL стане доступним для читання.

**`PGSQL_POLLING_WRITING`** (int)

Повертається функцією [пгconnectpoll()](function.pg-connect-poll.html) і вказує на те, що з'єднання очікує, коли сокет PostgreSQL стане доступним для запису.

**`PGSQL_POLLING_OK`** (int)

Повертається функцією [пгconnectpoll()](function.pg-connect-poll.html) і вказує на те, що з'єднання готове до використання.

**`PGSQL_POLLING_ACTIVE`** (int)

Повертається функцією [пгconnectpoll()](function.pg-connect-poll.html) і свідчить про те, що з'єднання зараз активно.

**`PGSQL_DIAG_SEVERITY_NONLOCALIZED`** (int)

Важливість; Можливі наступні значення: ERROR, FATAL або PANIC (у повідомленні про помилку), або WARNING, NOTICE, DEBUG, INFO або LOG (у повідомленні про попередження). Це ідентично полю PGDIAGSEVERITY крім того, вміст не локалізовано. Доступно лише у версії 9.6 або новіші / PHP 7.3.0 або новіші.