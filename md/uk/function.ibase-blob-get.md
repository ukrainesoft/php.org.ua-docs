---
navigation:
  - function.ibase-blob-echo.md: « ibase\_blob\_echo
  - function.ibase-blob-import.md: ibase\_blob\_import »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_get

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_get — Отримує кількість байтів від відкритого BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_get(resource $blob_handle, int $len): string
```

Функція повертає не більше `len` байт із BLOB-об'єкта, який був відкритий для читання за допомогою [ibase\_blob\_open()](function.ibase-blob-open.md)

> **Зауваження** :
> 
> Неможливо прочитати з BLOB-об'єкта, який був відкритий для запису за допомогою [ibase\_blob\_create()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibase\_blob\_open()](function.ibase-blob-open.md)

`len`

Розмір даних, що повертаються.

### Значення, що повертаються

Повертає не більше `len` байт із BLOB-об'єкта або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ibase\_blob\_get()\*\*\*\*

```php
<?php
$result    = ibase_query("SELECT blob_value FROM table");
$data      = ibase_fetch_object($result);
$blob_data = ibase_blob_info($data->BLOB_VALUE);
$blob_hndl = ibase_blob_open($data->BLOB_VALUE);
echo         ibase_blob_get($blob_hndl, $blob_data[0]);
?>
```

Хоча цей приклад робить не більше, ніж 'ibase\_blob\_echo($data->BLOB\_VALUE)', він показує, як отримати інформацію в $variable для подальших маніпуляцій.

### Дивіться також

-   [ibase\_blob\_open()](function.ibase-blob-open.md) \- Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_echo()](function.ibase-blob-echo.md) \- Виводить вміст BLOB-об'єкта у браузер
