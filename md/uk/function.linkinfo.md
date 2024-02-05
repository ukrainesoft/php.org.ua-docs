---
navigation:
  - function.link.md: « link
  - function.lstat.md: lstat »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: linkinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# linkinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

linkinfo — Повертає інформацію про посилання

### Опис

```methodsynopsis
linkinfo(string $path): int|false
```

Повертає інформацію про посилання.

Ця функція використовується для визначення, чи існує посилання (на яку вказує `path`) насправді (використовуючи той же метод, що і макрос S\_ISLNK, визначений у stat.h).

### Список параметрів

`path`

Шлях до заслання.

### Значення, що повертаються

**linkinfo()** повертає поле `st_dev` структури stat з Unix C, яку повертає системний виклик `lstat`. Повертає невід'ємне ціле число у разі успішного виконання, -1 у випадку, якщо посилання не було знайдено, або \*\*`false`\*\*в случае возникновения ошибки open.base\_dir.

### Приклади

**Приклад #1 Приклад использования функции**linkinfo()\*\*\*\*

```php
<?php

echo linkinfo('/vmlinuz'); // 835

?>
```

### Дивіться також

-   [symlink()](function.symlink.md) \- Створює символічне посилання
-   [link()](function.link.md) \- Створює жорстке посилання
-   [readlink()](function.readlink.md) \- Повертає файл, на який вказує символічне посилання
