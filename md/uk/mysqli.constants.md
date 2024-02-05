---
navigation:
  - mysqli.persistconns.md: Модуль mysqli та постійні з'єднання
  - mysqli.summary.md: Основна інформація про функції модуля MySQLi »
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`MYSQLI_READ_DEFAULT_GROUP`**(int)

Читати опції із зазначеної групи у файлі my.cnf або файлі, вказаному за допомогою **`MYSQLI_READ_DEFAULT_FILE`**

**`MYSQLI_READ_DEFAULT_FILE`**(int)

Читати опції із зазначеного файлу замість my.cnf

**`MYSQLI_OPT_CONNECT_TIMEOUT`**(int)

Час очікування на підключення в секундах.

**`MYSQLI_OPT_READ_TIMEOUT`**(int)

Час очікування результату виконання команди за секунди. Доступно з PHP 7.2.0.

**`MYSQLI_OPT_LOCAL_INFILE`**(int)

Включає команду `LOAD LOCAL INFILE`

**`MYSQLI_OPT_INT_AND_FLOAT_NATIVE`**(int)

Перетворює цілі та плаваючі стовпці назад у числа PHP. Коректно працює лише з mysqlnd.

**`MYSQLI_OPT_NET_CMD_BUFFER_SIZE`**(int)

Розмір внутрішнього буфера команди/мережі. Коректно працює лише з mysqlnd.

**`MYSQLI_OPT_NET_READ_BUFFER_SIZE`**(int)

Максимальний розмір блоку читання в байтах під час читання тіла пакета команд MySQL. Тільки valid для mysqlnd.

**`MYSQLI_OPT_SSL_VERIFY_SERVER_CERT`**(int)

Потрібно MySQL 5.1.10 і вище

**`MYSQLI_INIT_COMMAND`**(int)

Команда, яка буде виконана за умови підключення до сервера MySQL. Ця команда буде повторно викликана під час перепідключення.

**`MYSQLI_CLIENT_SSL`**(int)

Використовувати SSL (шифрований протокол). Ця опція не може бути встановлена ​​програмами; вона встановлюється усередині бібліотеки клієнта MySQL.

**`MYSQLI_CLIENT_COMPRESS`**(int)

Використовувати компресію.

**`MYSQLI_CLIENT_INTERACTIVE`**(int)

Чекати `interactive_timeout`секунд (вместо`wait_timeout`) бездіяльності перед закриттям з'єднання. Змінна сесії клієнта `wait_timeout`будет установлена в значение переменной сессии`interactive_timeout`

**`MYSQLI_CLIENT_IGNORE_SPACE`**(int)

Дозволити пробіли після назв функцій. Робить усі імена функцій зарезервованими словами.

**`MYSQLI_CLIENT_NO_SCHEMA`**(int)

Запретить синтаксис`db_name.tbl_name.col_name`

**`MYSQLI_CLIENT_MULTI_QUERIES`**

Дозволити виконання в одному дзвінку функції [mysqli\_query()](mysqli.query.md) кількох запитів, розділених крапкою з комою.

**`MYSQLI_STORE_RESULT`**(int)

Для буферизації наборів даних. Значення дорівнює

**`MYSQLI_USE_RESULT`**(int)

Для використання небуферизованих наборів даних. Значення дорівнює

**`MYSQLI_ASSOC`**(int)

Результат повертається у вигляді асоціативного масиву з іменами полів як індекси.

**`MYSQLI_NUM`**(int)

Результат повертається як індексного масиву.

**`MYSQLI_BOTH`**(int)

Результат повертається у вигляді масиву, що містить як числовий, так і асоціативний індекси.

**`MYSQLI_NOT_NULL_FLAG`**(int)

Повідомляє про те, що поле визначено як `NOT NULL`

**`MYSQLI_PRI_KEY_FLAG`**(int)

Поле є частиною первинного індексу.

**`MYSQLI_UNIQUE_KEY_FLAG`**(int)

Поле є частиною унікального індексу.

**`MYSQLI_MULTIPLE_KEY_FLAG`**(int)

Поле є частиною індексу.

**`MYSQLI_BLOB_FLAG`**(int)

Поле определено как`BLOB`

**`MYSQLI_UNSIGNED_FLAG`**(int)

Поле определено как`UNSIGNED`

**`MYSQLI_ZEROFILL_FLAG`**(int)

Поле определено как`ZEROFILL`

**`MYSQLI_AUTO_INCREMENT_FLAG`**(int)

Поле определено как`AUTO_INCREMENT`

**`MYSQLI_TIMESTAMP_FLAG`**(int)

Поле определено как`TIMESTAMP`

**`MYSQLI_SET_FLAG`**(int)

Поле определено как`SET`

**`MYSQLI_NUM_FLAG`**(int)

Поле определено как`NUMERIC`

**`MYSQLI_PART_KEY_FLAG`**(int)

Поле є частиною мульти-індексу.

**`MYSQLI_GROUP_FLAG`**(int)

Поле является частью`GROUP BY`

**`MYSQLI_TYPE_DECIMAL`**(int)

Поле определено как`DECIMAL`

**`MYSQLI_TYPE_NEWDECIMAL`**(int)

Математична точність полів `DECIMAL`или`NUMERIC` (MySQL 5.0.3 та вище).

**`MYSQLI_TYPE_BIT`**(int)

Поле определено как`BIT` (MySQL 5.0.3 та вище).

**`MYSQLI_TYPE_TINY`**(int)

Поле определено как`TINYINT`

**`MYSQLI_TYPE_SHORT`**(int)

Поле определено как`SMALLINT`

**`MYSQLI_TYPE_LONG`**(int)

Поле определено как`INT`

**`MYSQLI_TYPE_FLOAT`**(int)

Поле определено как`FLOAT`

**`MYSQLI_TYPE_DOUBLE`**(int)

Поле определено как`DOUBLE`

**`MYSQLI_TYPE_NULL`**(int)

Поле определено как`DEFAULT NULL`

**`MYSQLI_TYPE_TIMESTAMP`**(int)

Поле определено как`TIMESTAMP`

**`MYSQLI_TYPE_LONGLONG`**(int)

Поле определено как`BIGINT`

**`MYSQLI_TYPE_INT24`**(int)

Поле определено как`MEDIUMINT`

**`MYSQLI_TYPE_DATE`**(int)

Поле определено как`DATE`

**`MYSQLI_TYPE_TIME`**(int)

Поле определено как`TIME`

**`MYSQLI_TYPE_DATETIME`**(int)

Поле определено как`DATETIME`

**`MYSQLI_TYPE_YEAR`**(int)

Поле определено как`YEAR`

**`MYSQLI_TYPE_NEWDATE`**(int)

Поле определено как`DATE`

**`MYSQLI_TYPE_INTERVAL`**(int)

Поле определено как`INTERVAL`

**`MYSQLI_TYPE_ENUM`**(int)

Поле определено как`ENUM`

**`MYSQLI_TYPE_SET`**(int)

Поле определено как`SET`

**`MYSQLI_TYPE_TINY_BLOB`**(int)

Поле определено как`TINYBLOB`

**`MYSQLI_TYPE_MEDIUM_BLOB`**(int)

Поле определено как`MEDIUMBLOB`

**`MYSQLI_TYPE_LONG_BLOB`**(int)

Поле определено как`LONGBLOB`

**`MYSQLI_TYPE_BLOB`**(int)

Поле определено как`BLOB`

**`MYSQLI_TYPE_VAR_STRING`**(int)

Поле определено как`VARCHAR`

**`MYSQLI_TYPE_STRING`**(int)

Поле определено как`CHAR`или`BINARY`

**`MYSQLI_TYPE_CHAR`**(int)

Поле определено как`TINYINT`Для`CHAR`смотрите`MYSQLI_TYPE_STRING`

**`MYSQLI_TYPE_GEOMETRY`**(int)

Поле определено как`GEOMETRY`

**`MYSQLI_TYPE_JSON`**(int)

Поле определено как`JSON`. Дійсно тільки для MySQL і MySQL 5.7.8 і вище.

**`MYSQLI_NEED_DATA`**

Є ще дані, доступні для пов'язаних змінних.

**`MYSQLI_NO_DATA`**(int)

Більше немає доступних даних для пов'язаних змінних.

**`MYSQLI_DATA_TRUNCATED`**(int)

Відбулося усічення даних. Доступно з MySQL 5.0.5.

**`MYSQLI_ENUM_FLAG`**(int)

Поле определено как`ENUM`

**`MYSQLI_BINARY_FLAG`**(int)

Поле определено как`BINARY`

**`MYSQLI_CURSOR_TYPE_FOR_UPDATE`**(int)

**`MYSQLI_CURSOR_TYPE_NO_CURSOR`**(int)

**`MYSQLI_CURSOR_TYPE_READ_ONLY`**(int)

**`MYSQLI_CURSOR_TYPE_SCROLLABLE`**(int)

**`MYSQLI_STMT_ATTR_CURSOR_TYPE`**(int)

**`MYSQLI_STMT_ATTR_PREFETCH_ROWS`**(int)

**`MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH`**(int)

**`MYSQLI_SET_CHARSET_NAME`**(int)

**`MYSQLI_REPORT_INDEX`**(int)

Повідомляти, якщо індекс, який використовується у запиті, не вказано або перевищує максимум.

**`MYSQLI_REPORT_ERROR`**(int)

Повідомляти про помилки виклику mysqli.

**`MYSQLI_REPORT_STRICT`**(int)

Обробляти `mysqli_sql_exception`как ошибки, а не как предупреждения.

**`MYSQLI_REPORT_ALL`**(int)

Включити всі оповіщення.

**`MYSQLI_REPORT_OFF`**(int)

Вимикає повідомлення.

**`MYSQLI_DEBUG_TRACE_ENABLED`**(int)

Установлено в 1, если используется функция[mysqli\_debug()](mysqli.debug.md)

**`MYSQLI_SERVER_QUERY_NO_GOOD_INDEX_USED`**(int)

**`MYSQLI_SERVER_QUERY_NO_INDEX_USED`**(int)

**`MYSQLI_SERVER_PUBLIC_KEY`**(int)

**`MYSQLI_REFRESH_GRANT`**(int)

Оновлює таблицю прав доступу.

**`MYSQLI_REFRESH_LOG`**(int)

Скидає логи, так само, як і SQL вираз `FLUSH LOGS`

**`MYSQLI_REFRESH_TABLES`**(int)

Очищає кеш таблиці, так само, як і SQL вираз `FLUSH TABLES`

**`MYSQLI_REFRESH_HOSTS`**(int)

Очищає кеш хоста, так само, як і SQL вираз `FLUSH HOSTS`

**`MYSQLI_REFRESH_REPLICA`**(int)

Аліас константи **`MYSQLI_REFRESH_SLAVE`**. Доступна починаючи з PHP 8.1.0.

**`MYSQLI_REFRESH_STATUS`**(int)

Скидає змінні стани, так само, як і SQL вираз `FLUSH STATUS`

**`MYSQLI_REFRESH_THREADS`**(int)

Очищує кеш потоку.

**`MYSQLI_REFRESH_SLAVE`**(int)

На веденому сервері, що реплікується (slave): скинути інформацію провідного сервера (master) і перезапустити ведений сервер. Аналогічно до виконання SQL виразу `RESET SLAVE`

**`MYSQLI_REFRESH_MASTER`**(int)

На провідному сервері, що реплікується (master): видалити бінарні файли логів у бінарному індексі логів, і обрізати файл індексу. Аналогічно до виконання SQL виразу `RESET MASTER`

**`MYSQLI_TRANS_COR_AND_CHAIN`**(int)

Додає "AND CHAIN" у [mysqli\_commit()](mysqli.commit.md) або [mysqli\_rollback()](mysqli.rollback.md)

**`MYSQLI_TRANS_COR_AND_NO_CHAIN`**(int)

Додає "AND NO CHAIN" у [mysqli\_commit()](mysqli.commit.md) або [mysqli\_rollback()](mysqli.rollback.md)

**`MYSQLI_TRANS_COR_RELEASE`**(int)

Додає "RELEASE" в [mysqli\_commit()](mysqli.commit.md) або [mysqli\_rollback()](mysqli.rollback.md)

**`MYSQLI_TRANS_COR_NO_RELEASE`**(int)

Додає "NO RELEASE" в [mysqli\_commit()](mysqli.commit.md) або [mysqli\_rollback()](mysqli.rollback.md)

**`MYSQLI_TRANS_START_READ_ONLY`**(int)

Починає транзакцію як "START TRANSACTION READ ONLY" з [mysqli\_begin\_transaction()](mysqli.begin-transaction.md)

**`MYSQLI_TRANS_START_READ_WRITE`**(int)

Починає транзакцію як "START TRANSACTION READ WRITE" з [mysqli\_begin\_transaction()](mysqli.begin-transaction.md)

**`MYSQLI_TRANS_START_CONSISTENT_SNAPSHOT`**

Починає транзакцію як "START TRANSACTION WITH CONSISTENT SNAPSHOT" з [mysqli\_begin\_transaction()](mysqli.begin-transaction.md)

**`MYSQLI_CLIENT_SSL_DONT_VERIFY_SERVER_CERT`**(int)

Потрібен MySQL 5.6.5 і вище

**`MYSQLI_IS_MARIADB`**(bool)

Визначає, чи зібрано модуль mysqli з клієнтською бібліотекою MariaDB. Доступно з PHP 8.1.2.
