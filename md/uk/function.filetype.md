---
navigation:
  - function.filesize.md: « filesize
  - function.flock.md: flock »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: filetype
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

Повертає **`false`** у разі виникнення помилки . **filetype()** також викликає помилку рівня \*\*`E_NOTICE`\*\*якщо системний виклик stat завершиться помилкою або тип файлу невідомий.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання функції **filetype()****

```php
<?php

echo filetype('/etc/passwd');  // file
echo filetype('/etc/');        // dir

?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [ісdir()](function.is-dir.md) - Визначає, чи є ім'я файлу директорією
-   [ісfile()](function.is-file.md) - Визначає, чи файл є звичайним файлом
-   [ісlink()](function.is-link.md) - Визначає, чи є файл символічним посиланням
-   [fileexists()](function.file-exists.md) - Перевіряє існування вказаного файлу чи каталогу
-   [mimecontenttype()](function.mime-content-type.md) - Визначає MIME-тип вмісту файлу
-   [pathinfo()](function.pathinfo.md) - Повертає інформацію про шлях до файлу
-   [stat()](function.stat.md) - Повертає інформацію про файл
