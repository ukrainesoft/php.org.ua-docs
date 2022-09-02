---
navigation:
  - function.ibase-blob-echo.md: « ibaseblobecho
  - function.ibase-blob-import.md: ibaseblobimport »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseblobget
---
# ibaseblobget

(PHP 5, PHP 7 < 7.4.0)

ibaseblobget — Отримує кількість байтів від відкритого BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_get(resource $blob_handle, int $len): string
```

Функція повертає не більше `len` байт із BLOB-об'єкта, який був відкритий для читання за допомогою [ibaseblobopen()](function.ibase-blob-open.md)

> **Зауваження**
> 
> Неможливо прочитати з BLOB-об'єкта, який був відкритий для запису за допомогою [ibaseblobcreate()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibaseblobopen()](function.ibase-blob-open.md)

`len`

Розмір даних, що повертаються.

### Значення, що повертаються

Повертає не більше `len` байт із BLOB-об'єкта або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibaseblobget()****

```php
<?php
$result    = ibase_query("SELECT blob_value FROM table");
$data      = ibase_fetch_object($result);
$blob_data = ibase_blob_info($data->BLOB_VALUE);
$blob_hndl = ibase_blob_open($data->BLOB_VALUE);
echo         ibase_blob_get($blob_hndl, $blob_data[0]);
?>
```

Хоча цей приклад робить не більше, ніж 'ibaseblobecho($data->BLOBVALUE)', він показує, як отримати інформацію в $variable для подальших маніпуляцій.

### Дивіться також

-   [ibaseblobopen()](function.ibase-blob-open.md) - Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibaseblobclose()](function.ibase-blob-close.md) - Закриває BLOB-об'єкт
-   [ibaseblobecho()](function.ibase-blob-echo.md) - Виводить вміст BLOB-об'єкта у браузер
