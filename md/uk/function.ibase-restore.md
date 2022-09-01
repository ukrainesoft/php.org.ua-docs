---
navigation:
  - function.ibase-query.html: « ibasequery
  - function.ibase-rollback-ret.html: ibaserollbackret »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaserestore
---
# ibaserestore

(PHP 5, PHP 7 < 7.4.0)

ibaserestore — Запуск завдання відновлення в диспетчері служб і негайно повертається

### Опис

```methodsynopsis
ibase_restore(    resource $service_handle,    string $source_file,    string $dest_db,    int $options = 0,    bool $verbose = false): mixed
```

Ця функція передає аргументи (віддаленому) серверу бази даних. Там вона розпочинає новий процес відновлення. Тому ви не отримаєте жодної відповіді.

### Список параметрів

`service_handle`

Раніше відкрите з'єднання із сервером бази даних.

`source_file`

Абсолютний шлях на сервері, де є файл резервної копії.

`dest_db`

Шлях створення нової бази даних на сервері. Також можна використовувати псевдонім бази даних.

`options`

Додаткові параметри передачі на сервер бази даних для відновлення. Параметр `options` може бути комбінацією наступних констант: **`IBASE_RES_DEACTIVATE_IDX`** **`IBASE_RES_NO_SHADOW`** **`IBASE_RES_NO_VALIDITY`** **`IBASE_RES_ONE_AT_A_TIME`** **`IBASE_RES_REPLACE`** **`IBASE_RES_CREATE`** **`IBASE_RES_USE_ALL_SPACE`** **`IBASE_PRP_PAGE_BUFFERS`** **`IBASE_PRP_SWEEP_INTERVAL`** **`IBASE_RES_CREATE`**. Читайте розділ про [Обумовлені константи](ibase.constants.md) для отримання додаткової інформації.

`verbose`

Оскільки процес відновлення виконується на сервері бази даних, ви не зможете отримати висновок. Цей аргумент марний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Оскільки процес відновлення виконується на (віддаленому) сервері, ця функція просто передає йому аргументи. Якщо аргументи недійсні, то повернеться **`false`**

### Приклади

**Приклад #1 Приклад використання **ibaserestore()****

```php
<?php

// Подключение к серверу базы данных по ip-адресу и порту
$service = ibase_service_attach ('10.1.11.200/3050', 'sysdba', 'masterkey');

// Запуск процесса восстановления на сервере базы данных
// Восстановление резервной копии employee в новую базу данных emps.fdb
// Не используйте никаких специальных аргументов
ibase_restore($service, '/srv/backup/employees.fbk', '/srv/firebird/emps.fdb');

// Освобождение соединения
ibase_service_detach ($service);
?>
```

**Приклад #2 Приклад використання **ibaserestore()** з аргументами**

```php
<?php

// Присоединение к серверу базы данных по имени и порту по умолчанию
$service = ibase_service_attach ('fb-server.contoso.local', 'sysdba', 'masterkey');

// Запуск процесса восстановления на сервере базы данных
// Восстановление базы данных employee с использованием псевдонима.
// Восстановление без индексов. Замена существующей базы данных.
ibase_restore($service, '/srv/backup/employees.fbk', 'employees.fdb', IBASE_RES_DEACTIVATE_IDX | IBASE_RES_REPLACE);

// Освобождение прикрепленного соединения
ibase_service_detach ($service);
?>
```

### Дивіться також

-   [ibasebackup()](function.ibase-backup.html) - Ініціює завдання резервного копіювання у диспетчері служб та негайно повертає
