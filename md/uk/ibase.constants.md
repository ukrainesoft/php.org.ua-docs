Обумовлені константи

-   [« Типы ресурсов](ibase.resources.html)
    
-   [Функции Firebird/InterBase »](ref.ibase.html)
    
-   [PHP Manual](index.html)
    
-   [Firebird/InterBase](book.ibase.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

Наступні константи можна задавати у функції [ibase\_trans()](function.ibase-trans.html) визначення поведінки транзакцій.

**Прапори транзакцій Firebird/InterBase**

| Константа        | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IBASEDEFAULT     | Налаштування за промовчанням для нової транзакції. Це значення визначається клієнтською бібліотекою, яке в більшості випадків дорівнює IBASEWRITE                                                                                                                                                                                                                                                                                                                     |
| IBASEREAD        | Починає транзакцію лише на читання.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IBASEWRITE       | Починає транзакцію у режимі читання та запису.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| IBASECONSISTENCY | Починає транзакцію з рівнем ізоляції 'consistency' (узгодження). Це означає, що транзакція не може читати з таблиць, які вносяться зміни паралельними (конкуруючими) транзакціями.                                                                                                                                                                                                                                                                                    |
| IBASECONCURRENCY | Починає транзакцію з рівнем ізоляції 'concurrency' (або 'snapshot', 'миттєвий знімок'). Це означає, що транзакція має доступ до всіх таблиць, але може бачити зміни інших транзакцій після знімка.                                                                                                                                                                                                                                                                    |
| IBASECOMMITTED   | Починає транзакцію із рівнем ізоляції 'read committed' (читати фіксоване). Цей прапор має бути об'єднаний з **`IBASE_REC_VERSION`** або **`IBASE_REC_NO_VERSION`**. Цей рівень ізоляції дозволяє отримати доступ до змін, здійснених після початку транзакції. Якщо вказано прапор **`IBASE_REC_NO_VERSION`**, тільки остання версія змін може бути прочитана. Якщо вказано прапор **`IBASE_REC_VERSION`**, можна читати зміни, що у черзі у паралельних транзакціях. |
| IBASEWAIT        | Прапор, що вказує, що транзакція повинна чекати у разі конфлікту транзакцій.                                                                                                                                                                                                                                                                                                                                                                                          |
| IBASENOWAIT      | Прапор, що вказує на те, що транзакція повинна повернути помилку при виникненні конфлікту транзакцій.                                                                                                                                                                                                                                                                                                                                                                 |

Наступні константи можна задавати у функціях [ibase\_fetch\_row()](function.ibase-fetch-row.html) [ibase\_fetch\_assoc()](function.ibase-fetch-assoc.html) або [ibase\_fetch\_object()](function.ibase-fetch-object.html)для управління поведінкою вилученням даних.

**Прапори вилучення Firebird/InterBase**

| Константа        | Описание                                                                                                                                                                                                                       |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IBASEFETCHBLOBS  | Також можна використовувати **`IBASE_TEXT`** для забезпечення зворотної сумісності. Вимушує витягувати об'єкти BLOB повністю, а не лише їхні ідентифікатори.                                                                   |
| IBASEFETCHARRAYS | Вимушує витягувати масиви повністю, а не лише їх ідентифікатори. Ідентифікатори масивів можна використовувати тільки для операцій вставки, тому що на даний момент відсутні будь-які інші функції для роботи з ними.           |
| IBASEUNIXTIME    | Вимушує поля типу дата/час витягуватися не як рядки, а як тимчасові мітки Unix (кількість секунд, що пройшли з 1 січня 1970 00:00 UTC). Може викликати проблеми на деяких системах, якщо необхідно працювати з ранніми датами. |

Наступні константи використовуються для передачі запитів і сервісних функцій API ([ibase\_server\_info()](function.ibase-server-info.html) [ibase\_db\_info()](function.ibase-db-info.html) [ibase\_backup()](function.ibase-backup.html) [ibase\_restore()](function.ibase-restore.html) і [ibase\_maintain\_db()](function.ibase-maintain-db.html)). За подробицями зверніться до документації Firebird/InterBase.

**`IBASE_BKP_IGNORE_CHECKSUMS`**

**`IBASE_BKP_IGNORE_LIMBO`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_BKP_METADATA_ONLY`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_BKP_NO_GARBAGE_COLLECT`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_BKP_OLD_DESCRIPTIONS`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_BKP_NON_TRANSPORTABLE`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_BKP_CONVERT`**

Опція для [ibase\_backup()](function.ibase-backup.html)

**`IBASE_RES_DEACTIVATE_IDX`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_RES_NO_SHADOW`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_RES_NO_VALIDITY`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_RES_ONE_AT_A_TIME`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_RES_REPLACE`**

**`IBASE_RES_CREATE`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_RES_USE_ALL_SPACE`**

Опція для [ibase\_restore()](function.ibase-restore.html)

**`IBASE_PRP_PAGE_BUFFERS`**

**`IBASE_PRP_SWEEP_INTERVAL`**

**`IBASE_PRP_SHUTDOWN_DB`**

**`IBASE_PRP_DENY_NEW_TRANSACTIONS`**

**`IBASE_PRP_DENY_NEW_ATTACHMENTS`**

**`IBASE_PRP_RESERVE_SPACE`**

**`IBASE_PRP_RES_USE_FULL`**

**`IBASE_PRP_RES`**

**`IBASE_PRP_WRITE_MODE`**

**`IBASE_PRP_WM_ASYNC`**

**`IBASE_PRP_WM_SYNC`**

**`IBASE_PRP_ACCESS_MODE`**

**`IBASE_PRP_AM_READONLY`**

**`IBASE_PRP_AM_READWRITE`**

**`IBASE_PRP_SET_SQL_DIALECT`**

**`IBASE_PRP_ACTIVATE`**

**`IBASE_PRP_DB_ONLINE`**

**`IBASE_RPR_CHECK_DB`**

**`IBASE_RPR_IGNORE_CHECKSUM`**

**`IBASE_RPR_KILL_SHADOWS`**

**`IBASE_RPR_MEND_DB`**

**`IBASE_RPR_VALIDATE_DB`**

**`IBASE_RPR_FULL`**

**`IBASE_RPR_SWEEP_DB`**

Опція для [ibase\_maintain\_db()](function.ibase-maintain-db.html)

**`IBASE_STS_DATA_PAGES`**

**`IBASE_STS_DB_LOG`**

**`IBASE_STS_HDR_PAGES`**

**`IBASE_STS_IDX_PAGES`**

**`IBASE_STS_SYS_RELATIONS`**

Опція для [ibase\_db\_info()](function.ibase-db-info.html)

**`IBASE_SVC_SERVER_VERSION`**

Опція для [ibase\_server\_info()](function.ibase-server-info.html)

**`IBASE_SVC_IMPLEMENTATION`**

Опція для [ibase\_server\_info()](function.ibase-server-info.html)

**`IBASE_SVC_GET_ENV`**

Опція для [ibase\_server\_info()](function.ibase-server-info.html)

**`IBASE_SVC_GET_ENV_LOCK`**

**`IBASE_SVC_GET_ENV_MSG`**

**`IBASE_SVC_USER_DBPATH`**

**`IBASE_SVC_SVR_DB_INFO`**

**`IBASE_SVC_GET_USERS`**

Опція для [ibase\_server\_info()](function.ibase-server-info.html)