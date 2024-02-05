---
navigation:
  - function.filesize.md: « filesize
  - function.flock.md: flock »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: filetype
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filetype

(PHP 4, PHP 5, PHP 7, PHP 8)

filetype — Повертає тип файлу

### Опис

```methodsynopsis
filetype(string $filename): string|false
```

Повертає тип файлу.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає тип файлу. Можливими значеннями є fifo, char, dir, block, link, file, socket та unknown.

Повертає **`false`**в случае возникновения ошибки**filetype()** також викликає помилку рівня \*\*`E_NOTICE`\*\*якщо системний виклик stat завершиться помилкою або тип файлу невідомий.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання функції** filetype()\*\*\*\*

```php
<?php

echo filetype('/etc/passwd');
echo "\n";
echo filetype('/etc/');
?>
```

Результат виконання наведеного прикладу:

```
file
dir
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), смотрите в разделе[Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [is\_dir()](function.is-dir.md) \- Визначає, чи є ім'я файлу директорією
-   [is\_file()](function.is-file.md) \- Визначає, чи файл є звичайним файлом
-   [is\_link()](function.is-link.md) \- Визначає, чи є файл символічним посиланням
-   [file\_exists()](function.file-exists.md) \- Перевіряє існування вказаного файлу чи каталогу
-   [mime\_content\_type()](function.mime-content-type.md) \- Визначає MIME-тип вмісту файлу
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
-   [stat()](function.stat.md) \- Повертає інформацію про файл
