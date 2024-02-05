---
navigation:
  - ibase.resources.md: « Типи ресурсів
  - ref.ibase.md: Функції Firebird/InterBase »
  - index.md: PHP Manual
  - book.ibase.md: Firebird/InterBase
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Наступні константи можна задавати у функції [ibase\_trans()](function.ibase-trans.md)для определения поведения транзакций.

**Прапори транзакцій Firebird/InterBase**

| Константа | Опис |
| --- | --- |
| IBASE\_DEFAULT | Налаштування за промовчанням для нової транзакції. Це значення визначається клієнтською бібліотекою, яке в більшості випадків дорівнює IBASE\_WRITE |
| IBASE\_READ | Починає транзакцію лише на читання. |
| IBASE\_WRITE | Починає транзакцію у режимі читання та запису. |
| IBASE\_CONSISTENCY | Починає транзакцію з рівнем ізоляції 'consistency' (узгодження). Це означає, що транзакція не може читати з таблиць, які вносяться зміни паралельними (конкуруючими) транзакціями. |
| IBASE\_CONCURRENCY | Починає транзакцію з рівнем ізоляції 'concurrency' (або 'snapshot', 'миттєвий знімок'). Це означає, що транзакція має доступ до всіх таблиць, але може бачити зміни інших транзакцій після знімка. |
| IBASE\_COMMITTED | Починає транзакцію із рівнем ізоляції 'read committed' (читати фіксоване). Цей прапор має бути об'єднаний з **`IBASE_REC_VERSION`** або **`IBASE_REC_NO_VERSION`**. . Цей рівень ізоляції дозволяє отримати доступ до змін, здійснених після початку транзакції. Якщо вказано прапор **`IBASE_REC_NO_VERSION`**, тільки остання версія змін може бути прочитана. Якщо вказано прапор **`IBASE_REC_VERSION`**, можна читати зміни, що у черзі у паралельних транзакціях. |
| IBASE\_WAIT | Прапор, що вказує, що транзакція повинна чекати у разі конфлікту транзакцій. |
| IBASE\_NOWAIT | Прапор, що вказує на те, що транзакція повинна повернути помилку при виникненні конфлікту транзакцій. |

Наступні константи можна задавати у функціях [ibase\_fetch\_row()](function.ibase-fetch-row.md) [ibase\_fetch\_assoc()](function.ibase-fetch-assoc.md) або [ibase\_fetch\_object()](function.ibase-fetch-object.md)для управління поведінкою вилученням даних.

**Прапори вилучення Firebird/InterBase**

| Константа | Опис |
| --- | --- |
| IBASE\_FETCH\_BLOBS | Також можна використовувати **`IBASE_TEXT`** для забезпечення зворотної сумісності. Вимушує витягувати об'єкти BLOB повністю, а не лише їх ідентифікатори. |
| IBASE\_FETCH\_ARRAYS | Вимушує витягувати масиви цілком, а не лише їхні ідентифікатори. Ідентифікатори масивів можна використовувати тільки для операцій вставки, оскільки на даний момент відсутні будь-які інші функції для роботи з ними. |
| IBASE\_UNIXTIME | Вимушує поля типу дата/час витягуватися не як рядки, а як тимчасові мітки Unix (кількість секунд, що пройшли з 1 січня 1970 00:00 UTC). Може викликати проблеми на деяких системах, якщо необхідно працювати з ранніми датами. |

Наступні константи використовуються для передачі запитів і сервісних функцій API ([ibase\_server\_info()](function.ibase-server-info.md) [ibase\_db\_info()](function.ibase-db-info.md) [ibase\_backup()](function.ibase-backup.md) [ibase\_restore()](function.ibase-restore.md) і [ibase\_maintain\_db()](function.ibase-maintain-db.md)). За подробицями зверніться до документації Firebird/InterBase.

**`IBASE_BKP_IGNORE_CHECKSUMS`**

**`IBASE_BKP_IGNORE_LIMBO`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_BKP_METADATA_ONLY`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_BKP_NO_GARBAGE_COLLECT`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_BKP_OLD_DESCRIPTIONS`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_BKP_NON_TRANSPORTABLE`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_BKP_CONVERT`**

Опция для[ibase\_backup()](function.ibase-backup.md)

**`IBASE_RES_DEACTIVATE_IDX`**

Опция для[ibase\_restore()](function.ibase-restore.md)

**`IBASE_RES_NO_SHADOW`**

Опция для[ibase\_restore()](function.ibase-restore.md)

**`IBASE_RES_NO_VALIDITY`**

Опция для[ibase\_restore()](function.ibase-restore.md)

**`IBASE_RES_ONE_AT_A_TIME`**

Опция для[ibase\_restore()](function.ibase-restore.md)

**`IBASE_RES_REPLACE`**

**`IBASE_RES_CREATE`**

Опция для[ibase\_restore()](function.ibase-restore.md)

**`IBASE_RES_USE_ALL_SPACE`**

Опция для[ibase\_restore()](function.ibase-restore.md)

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

Опция для[ibase\_maintain\_db()](function.ibase-maintain-db.md)

**`IBASE_STS_DATA_PAGES`**

**`IBASE_STS_DB_LOG`**

**`IBASE_STS_HDR_PAGES`**

**`IBASE_STS_IDX_PAGES`**

**`IBASE_STS_SYS_RELATIONS`**

Опция для[ibase\_db\_info()](function.ibase-db-info.md)

**`IBASE_SVC_SERVER_VERSION`**

Опция для[ibase\_server\_info()](function.ibase-server-info.md)

**`IBASE_SVC_IMPLEMENTATION`**

Опция для[ibase\_server\_info()](function.ibase-server-info.md)

**`IBASE_SVC_GET_ENV`**

Опция для[ibase\_server\_info()](function.ibase-server-info.md)

**`IBASE_SVC_GET_ENV_LOCK`**

**`IBASE_SVC_GET_ENV_MSG`**

**`IBASE_SVC_USER_DBPATH`**

**`IBASE_SVC_SVR_DB_INFO`**

**`IBASE_SVC_GET_USERS`**

Опция для[ibase\_server\_info()](function.ibase-server-info.md)
