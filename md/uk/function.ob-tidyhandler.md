---
navigation:
  - ref.tidy.md: « Tidy
  - function.tidy-access-count.md: tidy\_access\_count »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: ob\_tidyhandler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_tidyhandler

(PHP 5, PHP 7, PHP 8)

ob\_tidyhandler — Функція зворотного дзвінка ob\_start для відновлення буфера

### Опис

```methodsynopsis
ob_tidyhandler(string $input, int $mode = ?): string
```

Функція зворотного дзвінка [ob\_start()](function.ob-start.md)для восстановление буфера.

### Список параметрів

`input`

Буфер.

`mode`

Режим буфера

### Значення, що повертаються

Повертає видозмінений буфер.

### Приклади

**Приклад #1 Приклад використання** ob\_tidyhandler()\*\*\*\*

```php
<?php
ob_start('ob_tidyhandler');

echo '<p>test</i>';
?>
```

Результат виконання наведеного прикладу:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html>
<head>
<title></title>
</head>
<body>
<p>test</p>
</body>
</html>
```

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
