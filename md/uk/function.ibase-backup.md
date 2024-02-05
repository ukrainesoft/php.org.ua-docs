---
navigation:
  - function.ibase-affected-rows.md: « ibase\_affected\_rows
  - function.ibase-blob-add.md: ibase\_blob\_add »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_backup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_backup

(PHP 5, PHP 7 < 7.4.0)

ibase\_backup — Ініціює завдання резервного копіювання у диспетчері служб та негайно повертає

### Опис

```methodsynopsis
ibase_backup(    resource $service_handle,    string $source_db,    string $dest_file,    int $options = 0,    bool $verbose = false): mixed
```

Ця функція передає аргументи на (віддалений) сервер бази даних. Там розпочинається новий процес резервного копіювання. Тому ви не отримаєте жодних відповідей.

### Список параметрів

`service_handle`

Раніше відкрите з'єднання із сервером бази даних.

`source_db`

Абсолютний шлях файлу бази даних на сервері бази даних. Також можна використовувати псевдонім бази даних.

`dest_file`

Шлях до файлу резервної копії на сервері бази даних.

`options`

Додаткові опції передачі на сервер бази даних для резервного копіювання. Параметр `options` може бути комбінацією з наступних констант: **`IBASE_BKP_IGNORE_CHECKSUMS`** **`IBASE_BKP_IGNORE_LIMBO`** **`IBASE_BKP_METADATA_ONLY`** **`IBASE_BKP_NO_GARBAGE_COLLECT`** **`IBASE_BKP_OLD_DESCRIPTIONS`** \*\*`IBASE_BKP_NON_TRANSPORTABLE`**или**`IBASE_BKP_CONVERT`\*\*Прочтите раздел о [Обумовлені константи](ibase.constants.md) для отримання додаткової інформації.

`verbose`

Оскільки процес резервного копіювання виконується на сервері бази даних, ви не маєте шансів отримати його висновок. Цей аргумент марний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Оскільки процес резервного копіювання виконується на (віддаленому) сервері, ця функція просто передає йому аргументи. Поки аргументи коректні, ви не отримаєте **`false`**

### Приклади

**Пример #1 Пример использования**ibase\_backup()\*\*\*\*

```php
<?php

// Соединение к серверу базы данных по IP-адресу и порту
$service = ibase_service_attach ('10.1.11.200/3050', 'sysdba', 'masterkey');

// Запуск процесса резервного копирования на сервере базы данных
// Резервное копирование базы данных сотрудников, используя полный путь к /srv/backup/employees.fbk
// Не используйте никаких специальных аргументов
ibase_backup($service, '/srv/firebird/employees.fdb', '/srv/backup/employees.fbk');

// Освобождение подключённого соединения
ibase_service_detach ($service);
?>
```

**Пример #2 Пример использования**ibase\_backup()\*\* з аргументами\*\*

```php
<?php

// Подключиться к серверу базы данных по имени и порту по умолчанию
$service = ibase_service_attach ('fb-server.contoso.local', 'sysdba', 'masterkey');

// Запуск процесс резервного копирования на сервере базы данных
// Резервное копирование базы данных сотрудников с использованием псевдонима в /srv/backup/employees.fbk.
// Резервное копирование только метаданных. Не создавайте переносную резервную копию.
ibase_backup($service, 'employees.fdb', '/srv/backup/employees.fbk', IBASE_BKP_METADATA_ONLY | IBASE_BKP_NON_TRANSPORTABLE);

// Освобождение подключённого соединения
ibase_service_detach ($service);
?>
```

### Дивіться також

-   [ibase\_restore()](function.ibase-restore.md) \- Запускає завдання відновлення у диспетчері служб та негайно повертається
