---
navigation:
  - sqlsrv.resources.md: « Типи ресурсів
  - ref.sqlsrv.md: Функції SQLSRV »
  - index.md: PHP Manual
  - book.sqlsrv.md: SQLSRV
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SQLSRV_FETCH_ASSOC`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.md) повертати асоціативний масив.

**`SQLSRV_FETCH_NUMERIC`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.md) повертати масив із числовими ключами.

**`SQLSRV_FETCH_BOTH`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.md) повертати масив з ключами та числовими та асоціативними (поведінка за умовчанням).

**`SQLSRV_ERR_ALL`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_errors()](function.sqlsrv-errors.md) повертати і помилки та попередження (поведінка за умовчанням).

**`SQLSRV_ERR_ERRORS`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_errors()](function.sqlsrv-errors.md) повертати лише помилки (без попереджень).

**`SQLSRV_ERR_WARNINGS`**(int)

Переданий як параметр, змушує функцію [sqlsrv\_errors()](function.sqlsrv-errors.md) повертати лише попередження (без помилок).

**`SQLSRV_LOG_SYSTEM_ALL`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md)включає журналування всіх підсистем.

**`SQLSRV_LOG_SYSTEM_CONN`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md)включає журналювання активності з'єднання.

**`SQLSRV_LOG_SYSTEM_INIT`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md)включає журналювання активності ініціалізації.

**`SQLSRV_LOG_SYSTEM_OFF`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), вимикає журнал усіх підсистем.

**`SQLSRV_LOG_SYSTEM_STMT`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md)включає журналювання активності виконання виразів (statement activity).

**`SQLSRV_LOG_SYSTEM_UTIL`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), включає журналювання активності функції помилок.

**`SQLSRV_LOG_SEVERITY_ALL`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), Визначає, що помилки, попередження та зауваження будуть журналюватися.

**`SQLSRV_LOG_SEVERITY_ERROR`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), Визначає, що помилки будуть журналюватися.

**`SQLSRV_LOG_SEVERITY_NOTICE`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), Визначає, що зауваження будуть журналюватися.

**`SQLSRV_LOG_SEVERITY_WARNING`**(int)

Переданий як параметр функції [sqlsrv\_configure()](function.sqlsrv-configure.md), Визначає, що попередження будуть журналюватися.

**`SQLSRV_NULLABLE_YES`**(int)

Показує, що значення шпальти може бути NULL.

**`SQLSRV_NULLABLE_NO`**(int)

Показує, що значення стовпця може бути NULL.

**`SQLSRV_NULLABLE_UNKNOWN`**(int)

Показує, що невідомо, чи значення стовпця може бути NULL.

**`SQLSRV_PARAM_IN`**(int)

При передаче в качестве параметра в функции[sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_prepare()](function.sqlsrv-prepare.md) показує, що параметр є вхідним.

**`SQLSRV_PARAM_INOUT`**(int)

При передаче в качестве параметра в функции[sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_prepare()](function.sqlsrv-prepare.md) показує, що параметр є вхідним і вихідним.

**`SQLSRV_PARAM_OUT`**(int)

При передаче в качестве параметра в функции[sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_prepare()](function.sqlsrv-prepare.md) показує, що параметр вихідним.

**`SQLSRV_PHPTYPE_INT`**(int)

Визначає цілий тип даних PHP (integer). За інформацією про використання зверніться до розділу документації [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_PHPTYPE_DATETIME`**(int)

Визначає часовий тип даних PHP (datetime). За інформацією про використання зверніться до розділу документації [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_PHPTYPE_FLOAT`**(int)

Визначає тип даних PHP з плаваючою точкою (float). За інформацією про використання зверніться до розділу документації [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_PHPTYPE_STREAM`**(int)

Визначає потік даних PHP (stream). Ця константа працює як функція та приймає константи кодувань. Дивіться константи виду SQLSRV\_ENC\_\*За информацией об использовании обратитесь к разделу документации[» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_PHPTYPE_STRING`**(int)

Визначає рядковий тип даних PHP (string). Ця константа працює як функція та приймає константи кодувань. Дивіться константи виду SQLSRV\_ENC\_\*За информацией об использовании обратитесь к разделу документации[» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_ENC_BINARY`**(int)

Визначає, що дані від сервера повертаються як потоку байтів без виконання кодування чи перетворення. За інформацією про використання зверніться до розділу [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_ENC_CHAR`**(int)

Дані повертаються у форматі восьмибітних символів як визначено кодову сторінку локалі Windows, встановленої в системі. Будь-які мультибайтові символи або символи, які не перетворюються на цю кодову сторінку, замінюються однобайтовим символом питання (?). Це кодування є кодуванням за замовчуванням. За інформацією про використання зверніться до розділу документації [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`UTF-8`**(int)

Визначає, що дані повертаються у кодуванні UTF-8. За інформацією про використання зверніться до розділу документації [» Визначення типів PHP](http://msdn.microsoft.com/en-us/library/cc296208.aspx)

**`SQLSRV_SQLTYPE_BIGINT`**(int)

Описує тип SQL BIGINT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_BINARY`**(int)

Описує SQL тип BINARY. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_BIT`**(int)

Описує SQL-тип BIT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_CHAR`**(int)

Описує тип SQL CHAR. Ця константа працює як функція і приймає один параметр, який визначає кількість символів. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_DATE`**(int)

Визначає SQL-тип DATE. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_DATETIME`**(int)

Описує SQL-тип DATETIME. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_DATETIME2`**(int)

Описує тип SQL DATETIME2. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_DATETIMEOFFSET`**(int)

Описує SQL-тип DATETIMEOFFSET. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_DECIMAL`**(int)

Описує SQL-тип DECIMAL. Ця константа працює як функція і приймає два параметри, що задає точність та розрядність. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_FLOAT`**(int)

Описує SQL-тип FLOAT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_IMAGE`**(int)

Описує SQL-тип IMAGE. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_INT`**(int)

Описує SQL-тип INT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_MONEY`**(int)

Описує SQL-тип MONEY. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_NCHAR`**(int)

Описує SQL-тип NCHAR. Ця константа працює як функція і приймає один параметр, який визначає кількість символів. За інформацією про використання зверніться до розділу документації [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_NUMERIC`**(int)

Описує тип NUMERIC. Ця константа працює як функція і приймає два параметри, що задає точність та розрядність. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_NVARCHAR`**(int)

Описує тип NVARCHAR. Ця константа працює як функція і приймає один параметр, який визначає кількість символів. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_NVARCHAR('max')`**(int)

Описує тип SQL NVARCHAR(MAX). За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_NTEXT`**(int)

Описує тип NTEXT SQL. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_REAL`**(int)

Описує SQL-тип REAL. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_SMALLDATETIME`**(int)

Описує тип SQL SMALLDATETIME. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_SMALLINT`**(int)

Описує тип SQL SMALLINT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_SMALLMONEY`**(int)

Описує SQL-тип SMALLMONEY. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_TEXT`**(int)

Описує SQL-тип TEXT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_TIME`**(int)

Описує SQL-тип TIME. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_TIMESTAMP`**(int)

Описує тип TIMESTAMP. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_TINYINT`**(int)

Описує тип TINYINT SQL. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_UNIQUEIDENTIFIER`**(int)

Описує SQL-тип UNIQUEIDENTIFIER. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_UDT`**(int)

Описує SQL-тип UDT. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_VARBINARY`**(int)

Описує тип SQL VARBINARY. Ця константа працює як функція та приймає один параметр, що задає кількість байт. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_VARBINARY('max')`**(int)

Описує тип SQL VARBINARY(MAX). За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_VARCHAR`**(int)

Описує тип VARCHAR. Ця константа працює як функція і приймає один параметр, який визначає кількість символів. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_VARCHAR('max')`**(int)

Описує тип SQL VARCHAR(MAX). За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_SQLTYPE_XML`**(int)

Описує SQL-тип XML. За інформацією про використання зверніться до розділу [» Визначення типів SQL](http://msdn.microsoft.com/en-us/library/cc626305.aspx)

**`SQLSRV_TXN_READ_UNCOMMITTED`**(int)

Встановлює рівень ізоляції транзакції рівним READ UNCOMMITTED. Це значення використовується для встановлення рівня TransactionIsolation у масиві $connectionOptions, переданому аргументом у функцію [sqlsrv\_connect()](function.sqlsrv-connect.md)

**`SQLSRV_TXN_READ_COMMITTED`**(int)

Встановлює рівень ізоляції транзакції рівним READ COMMITTED. Це значення використовується для встановлення рівня TransactionIsolation у масиві $connectionOptions, переданому аргументом у функцію [sqlsrv\_connect()](function.sqlsrv-connect.md)

**`SQLSRV_TXN_REPEATABLE_READ`**(int)

Задає рівень ізоляції транзакції рівним REPEATABLE READ. Це значення використовується для встановлення рівня TransactionIsolation у масиві $connectionOptions, переданому аргументом у функцію [sqlsrv\_connect()](function.sqlsrv-connect.md)

**`SQLSRV_TXN_SNAPSHOT`**(int)

Задає рівень ізоляції транзакції рівним SNAPSHOT. Це значення використовується для встановлення рівня TransactionIsolation у масиві $connectionOptions, переданому аргументом у функцію [sqlsrv\_connect()](function.sqlsrv-connect.md)

**`SQLSRV_TXN_READ_SERIALIZABLE`**(int)

Задає рівень ізоляції транзакції рівним SERIALIZABLE. Це значення використовується для встановлення рівня TransactionIsolation у масиві $connectionOptions, переданому аргументом у функцію [sqlsrv\_connect()](function.sqlsrv-connect.md)

**`SQLSRV_CURSOR_FORWARD`**(int)

Задає тип курсору як forward-only. За інформацією про використання зверніться до розділу [» Визначення типів курсорів](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_CURSOR_STATIC`**(int)

Задає тип курсору як static. За інформацією про використання зверніться до розділу [» Визначення типів курсорів](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_DYNAMIC`**(int)

Задає тип курсору як динамічний. За інформацією про використання зверніться до розділу [» Визначення типів курсорів](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_CURSOR_KEYSET`**(int)

Задає тип курсору як keyset. За інформацією про використання зверніться до розділу [» Визначення типів курсорів](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_CURSOR_BUFFERED`**(int)

Створює запит із курсором за клієнта. Дозволяє отримувати рядки у будь-якому порядку. За інформацією про використання зверніться до розділу [» Визначення типів курсорів](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_NEXT`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_PRIOR`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_FIRST`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_LAST`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_ABSOLUTE`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)

**`SQLSRV_SCROLL_RELATIVE`**(int)

Вказує, який рядок вибрати із результуючого набору. За інформацією про використання зверніться до розділу [» Визначення типів курсорів та вибірка рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)
