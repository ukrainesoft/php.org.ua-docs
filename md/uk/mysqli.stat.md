---
navigation:
  - mysqli.ssl-set.md: '« mysqli::ssl\_set'
  - mysqli.stmt-init.md: 'mysqli::stmt\_init »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::stat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::stat

# mysqli\_stat

(PHP 5, PHP 7, PHP 8)

mysqli::stat -- mysqli\_stat — Отримання інформації про поточний стан системи

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::stat(): string|false
```

Процедурний стиль

```methodsynopsis
mysqli_stat(mysqli $mysql): string|false
```

**mysqli\_stat()** повертає рядок з інформацією, схожою на ту, що надає команда 'mysqladmin status'. Сюди включається час роботи з моменту завантаження в секундах, кількість запущених процесів, запитів, перезавантажень та відкритих таблиць.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Рядок з інформацією про стан системи . \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysqli::stat()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

printf("System status: %s\n", $mysqli->stat());
?>
```

Процедурний стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

printf("System status: %s\n", mysqli_stat($link));
?>
```

Результат виконання наведених прикладів:

```
Состояние системы: Uptime: 272  Threads: 1  Questions: 5340  Slow queries: 0
Opens: 13  Flush tables: 1  Open tables: 0  Queries per second avg: 19.632
Memory in use: 8496K  Max memory used: 8560K
```

### Дивіться також

-   [mysqli\_get\_server\_info()](mysqli.get-server-info.md) \- Повертає версію MySQL сервера
