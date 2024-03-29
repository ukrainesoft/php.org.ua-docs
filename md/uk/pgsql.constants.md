---
navigation:
  - pgsql.resources.md: « Типи ресурсів
  - pgsql.examples.md: Приклади »
  - index.md: PHP Manual
  - book.pgsql.md: PostgreSQL
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`PGSQL_LIBPQ_VERSION`**(string)

Коротке позначення версії модуля libpq, що містить лише цифри та точки.

**`PGSQL_LIBPQ_VERSION_STR`**(string)

До PHP 8.0.0 — довге позначення версії модуля libpq, яке включає інформацію про компілятор. Починаючи з PHP 8.0.0, значення ідентичне **`PGSQL_LIBPQ_VERSION`**, а использование\*\*`PGSQL_LIBPQ_VERSION_STR`\*\*устарело.

**`PGSQL_ASSOC`**(int)

Передається у функцію [pg\_fetch\_array()](function.pg-fetch-array.md). . Повертає асоціативний масив 'ім'я поля' => 'значення поля'.

**`PGSQL_NUM`**(int)

Передається у функцію [pg\_fetch\_array()](function.pg-fetch-array.md). . Повертає нумерований масив 'номер поля' => 'значення поля'.

**`PGSQL_BOTH`**(int)

Передається у функцію [pg\_fetch\_array()](function.pg-fetch-array.md). Повертає масив значень поля, нумерований (за номером поля) та асоціативний (на ім'я поля).

**`PGSQL_CONNECT_FORCE_NEW`**(int)

Передається у функцію [pg\_connect()](function.pg-connect.md) для примусового створення нового з'єднання замість використання ідентичного існуючого.

**`PGSQL_CONNECT_ASYNC`**(int)

Передається у функцію [pg\_connect()](function.pg-connect.md) для створення асинхронного з'єднання.

**`PGSQL_CONNECTION_AUTH_OK`**(int)

**`PGSQL_CONNECTION_AWAITING_RESPONSE`**(int)

**`PGSQL_CONNECTION_BAD`**(int)

Повертається функцією [pg\_connection\_status()](function.pg-connection-status.md), вказує на непрацездатність з'єднання з базою даних

**`PGSQL_CONNECTION_MADE`**(int)

**`PGSQL_CONNECTION_OK`**(int)

Повертається функцією [pg\_connection\_status()](function.pg-connection-status.md), вказує на нормальний (робочий) стан з'єднання з базою даних

**`PGSQL_CONNECTION_SETENV`**(int)

**`PGSQL_CONNECTION_SSL_STARTUP`**(int)

**`PGSQL_CONNECTION_STARTED`**(int)

**`PGSQL_SEEK_SET`**(int)

Передається у функцію [pg\_lo\_seek()](function.pg-lo-seek.md). Операція пошуку розпочне роботу з початку об'єкта.

**`PGSQL_SEEK_CUR`**(int)

Передається у функцію [pg\_lo\_seek()](function.pg-lo-seek.md). Операція пошуку розпочне роботу з поточної позиції.

**`PGSQL_SEEK_END`**(int)

Передається у функцію [pg\_lo\_seek()](function.pg-lo-seek.md). Операція пошуку розпочне роботу з кінця об'єкта.

**`PGSQL_EMPTY_QUERY`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Означає, що відправлений на сервер рядок був порожнім.

**`PGSQL_COMMAND_OK`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Означає успішне завершення команди, яка не повертає дані.

**`PGSQL_TUPLES_OK`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Означає успішне завершення команди, яка повертає будь-які дані (наприклад, `SELECT`или`SHOW`

**`PGSQL_COPY_OUT`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Повідомляє, що було розпочато копіювання даних із сервера.

**`PGSQL_COPY_IN`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Повідомляє, щоб розпочато копіювання даних на сервер.

**`PGSQL_BAD_RESPONSE`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Повідомляє, що відповідь від сервера не розпізнано.

**`PGSQL_NONFATAL_ERROR`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Повідомляє, що виникла некритична (повідомлення чи попередження) помилка.

**`PGSQL_FATAL_ERROR`**(int)

Повертається функцією [pg\_result\_status()](function.pg-result-status.md). Повідомляє, що сталась критична помилка.

**`PGSQL_TRANSACTION_IDLE`**(int)

Повертається функцією [pg\_transaction\_status()](function.pg-transaction-status.md). Означає, що з'єднання на даний момент не діє і не знаходиться в рамках транзакції.

**`PGSQL_TRANSACTION_ACTIVE`**(int)

Повертається функцією [pg\_transaction\_status()](function.pg-transaction-status.md). Означає стан, коли команда перебуває у виконання. Запит через з'єднання надіслано, але виконання ще не завершено.

**`PGSQL_TRANSACTION_INTRANS`**(int)

Повертається функцією [pg\_transaction\_status()](function.pg-transaction-status.md). Це означає, що з'єднання простоює і знаходиться в рамках транзакції.

**`PGSQL_TRANSACTION_INERROR`**(int)

Повертається функцією [pg\_transaction\_status()](function.pg-transaction-status.md). Означає, що з'єднання простоює і знаходиться в рамках транзакції потерпілої під час виконання.

**`PGSQL_TRANSACTION_UNKNOWN`**(int)

Повертається функцією [pg\_transaction\_status()](function.pg-transaction-status.md). Означає, що з'єднання розірвано.

**`PGSQL_DIAG_SEVERITY`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Повідомляє про скруту. Можливі лише перелічені значення: `ERROR` `FATAL`, или`PANIC` (у повідомленні про помилку), або `WARNING` `NOTICE` `DEBUG` `INFO`, или`LOG` (у повідомленні), або переклад перерахованих значень відповідно до поточної локалізації. Поле завжди визначене.

**`PGSQL_DIAG_SQLSTATE`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Код помилки SQLSTATE. Код SQLSTATE визначає тип помилки, що відбулася; він може бути використаний прикладною програмою при виконанні специфічних операцій (таких як обробка помилки) у відповідь на помилку бази даних. Це поле завжди визначено та його значення не залежить від локалізації.

**`PGSQL_DIAG_MESSAGE_PRIMARY`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Основне легкочитане повідомлення про помилку (зазвичай один рядок). Поле завжди визначене.

**`PGSQL_DIAG_MESSAGE_DETAIL`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Деталізація: додаткове повідомлення про помилку, що містить докладнішу інформацію про проблему. Може містити кілька рядків.

**`PGSQL_DIAG_MESSAGE_HINT`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Підказка: вказівка ​​на можливі шляхи усунення помилки. Відрізняється від деталізації помилки тим, що це просто пропозиції (можливо помилкові), а чи не точна інформація. Може містити кілька рядків.

**`PGSQL_DIAG_STATEMENT_POSITION`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Рядок, що містить ціле десяткове число, що вказує на позицію курсора у вихідному виразі, в якому сталася помилка. Перший символ має індекс 1, позиції вимірюються в символах, а чи не в байтах.

**`PGSQL_DIAG_INTERNAL_POSITION`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Ця константа визначена так само, як поле \*\*`PG_DIAG_STATEMENT_POSITION`\*\*але цю константу застосовують, коли позиція курсору вказує на команду, згенеровану сервером БД. Поле **`PG_DIAG_INTERNAL_QUERY`** з'являтиметься щоразу, коли з'являється це поле.

**`PGSQL_DIAG_INTERNAL_QUERY`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Текст помилки, згенерованої внутрішньою командою СУБД, у якій сталася помилка. Це може бути, наприклад, SQL-запит, сформований функцією PL/pgSQL.

**`PGSQL_DIAG_CONTEXT`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Вказівка ​​на контекст, де сталася помилка. В основному містить трасування запрограмованих функцій та автоматично згенерованих запитів. Трасування виводиться рядково, починаючи з останнього рядка.

**`PGSQL_DIAG_SOURCE_FILE`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Ім'я файлу вихідного коду PostgreSQL, у якому зазначено помилку.

**`PGSQL_DIAG_SOURCE_LINE`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Номер рядка файлу вихідного коду PostgreSQL, де зазначено помилку.

**`PGSQL_DIAG_SOURCE_FUNCTION`**(int)

Передається у функцію [pg\_result\_error\_field()](function.pg-result-error-field.md). Ім'я функції у вихідному коді PostgreSQL, що повідомляє про помилку.

**`PGSQL_DIAG_SCHEMA_NAME`**(int)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_TABLE_NAME`**(int)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_COLUMN_NAME`**(int)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_DATATYPE_NAME`**(int)

Додано до PHP 7.3.0.

**`PGSQL_DIAG_CONSTRAINT_NAME`**(int)

Додано до PHP 7.3.0.

**`PGSQL_ERRORS_TERSE`**(int)

Передається у функцію [pg\_set\_error\_verbosity()](function.pg-set-error-verbosity.md). Дає припис, що повідомлення, що видаються, будуть містити тільки важливість помилки, основний текст і покажчик на місце, де вона відбулася; ця інформація зазвичай міститься в один рядок.

**`PGSQL_ERRORS_DEFAULT`**(int)

Передається у функцію [pg\_set\_error\_verbosity()](function.pg-set-error-verbosity.md). У режимі за промовчанням повідомлення про помилки містять описану вище інформацію, а також деталізацію, підказку або поля з контекстом помилки (можуть займати кілька рядків).

**`PGSQL_ERRORS_VERBOSE`**(int)

Передається у функцію [pg\_set\_error\_verbosity()](function.pg-set-error-verbosity.md). Задає режим, в якому у повідомлення будуть включені всі поля.

**`PGSQL_NOTICE_LAST`**(int)

Вказується у функції [pg\_last\_notice()](function.pg-last-notice.md)Доступно с PHP 7.1.0.

**`PGSQL_NOTICE_ALL`**(int)

Використовується [pg\_last\_notice()](function.pg-last-notice.md)Доступно с PHP 7.1.0.

**`PGSQL_NOTICE_CLEAR`**(int)

Використовується [pg\_last\_notice()](function.pg-last-notice.md)Доступно с PHP 7.1.0.

**`PGSQL_STATUS_LONG`**(int)

Передається у функцію [pg\_result\_status()](function.pg-result-status.md). Вказує на те, що як значення, що повертається, очікується числовий код.

**`PGSQL_STATUS_STRING`**(int)

Передається у функцію [pg\_result\_status()](function.pg-result-status.md). Вказує на те, що як значення, що повертається очікується текстове подання статусу.

**`PGSQL_CONV_IGNORE_DEFAULT`**(int)

Передається у функцію [pg\_convert()](function.pg-convert.md)Игнорировать значения по умолчанию в таблице в процессе преобразования.

**`PGSQL_CONV_FORCE_NULL`**(int)

Передається у функцію [pg\_convert()](function.pg-convert.md). Замінювати порожні рядки string на SQL `NULL`при преобразовании.

**`PGSQL_CONV_IGNORE_NOT_NULL`**(int)

Передається у функцію [pg\_convert()](function.pg-convert.md). Вказує, що не потрібно конвертувати **`null`** у стовпці SQL `NOT NULL`

**`PGSQL_DML_NO_CONV`**(int)

Передається у функцію [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md). Усі параметри передаються у вихідному вигляді. Ручне екранування обов'язково, якщо параметри містять дані користувача. Використовуйте для цього [pg\_escape\_string()](function.pg-escape-string.md)

**`PGSQL_DML_EXEC`**(int)

Передається у функцію [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md). Виконати запит за допомогою цих опцій.

**`PGSQL_DML_ASYNC`**(int)

Передається у функцію [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md). Виконайте асинхронний запит за допомогою цих функцій.

**`PGSQL_DML_STRING`**(int)

Передається у функцію [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md). Повернути рядок із виконаним запитом.

**`PGSQL_DML_ESCAPE`**(int)

Передається у функцію [pg\_insert()](function.pg-insert.md) [pg\_select()](function.pg-select.md) [pg\_update()](function.pg-update.md) і [pg\_delete()](function.pg-delete.md). Застосувати екранування до всіх параметрів замість внутрішнього виклику [pg\_convert()](function.pg-convert.md). Ця опція пропускає перегляд метаданих. Запит може бути таким самим швидким, як і [pg\_query()](function.pg-query.md) і [pg\_send\_query()](function.pg-send-query.md)

**`PGSQL_POLLING_FAILED`**(int)

Повертається функцією [pg\_connect\_poll()](function.pg-connect-poll.md) і свідчить про те, що спроба з'єднання провалилася.

**`PGSQL_POLLING_READING`**(int)

Повертається функцією [pg\_connect\_poll()](function.pg-connect-poll.md) і вказує на те, що з'єднання очікує, коли сокет PostgreSQL стане доступним для читання.

**`PGSQL_POLLING_WRITING`**(int)

Повертається функцією [pg\_connect\_poll()](function.pg-connect-poll.md) і вказує на те, що з'єднання очікує, коли сокет PostgreSQL стане доступним для запису.

**`PGSQL_POLLING_OK`**(int)

Повертається функцією [pg\_connect\_poll()](function.pg-connect-poll.md) і вказує на те, що з'єднання готове до використання.

**`PGSQL_POLLING_ACTIVE`**(int)

Повертається функцією [pg\_connect\_poll()](function.pg-connect-poll.md) і свідчить про те, що з'єднання зараз активно.

**`PGSQL_DIAG_SEVERITY_NONLOCALIZED`**(int)

Важливість; Можливі наступні значення: ERROR, FATAL або PANIC (у повідомленні про помилку), або WARNING, NOTICE, DEBUG, INFO або LOG (у повідомленні про попередження). Це ідентично полю PG\_DIAG\_SEVERITY крім того, вміст не локалізовано. Доступно лише у версії 9.6 або новіші / PHP 7.3.0 або новіші.

**`PGSQL_SHOW_CONTEXT_NEVER`**(int)

Константу вказують під час виклику функції [pg\_set\_error\_context\_visibility()](function.pg-set-error-context-visibility.md)приховує показ контексту. Доступна з PHP 8.3.0.

**`PGSQL_SHOW_CONTEXT_ERRORS`**(int)

Константу вказують під час виклику функції [pg\_set\_error\_context\_visibility()](function.pg-set-error-context-visibility.md), поля контексту будуть включені лише у повідомлення про помилки. Це стандартна поведінка. Доступна з PHP 8.3.0.

**`PGSQL_SHOW_CONTEXT_ALWAYS`**(int)

Константу вказують під час виклику функції [pg\_set\_error\_context\_visibility()](function.pg-set-error-context-visibility.md), поля контексту будуть включені в повідомлення про помилки, повідомлення та попередження. Доступна з PHP 8.3.0.

**`PGSQL_TRACE_SUPPRESS_TIMESTAMPS`**(int)

Константу вказують під час виклику функції [pg\_trace()](function.pg-trace.md), мітка часу не буде включена до повідомлення трасування. Доступна з PHP 8.3.0.

**`PGSQL_TRACE_REGRESS_MODE`**(int)

Константу вказують під час виклику функції [pg\_trace()](function.pg-trace.md), поля на кшталт OIDs будуть включені до повідомлення трасування. Доступна з PHP 8.3.0.
