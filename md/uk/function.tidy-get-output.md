---
navigation:
  - function.tidy-error-count.md: « tidy\_error\_count
  - function.tidy-warning-count.md: tidy\_warning\_count »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidy\_get\_output
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy\_get\_output

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy\_get\_output - Повертає рядок, що представляє розібрану tidy-розмітку

### Опис

```methodsynopsis
tidy_get_output(tidy $tidy): string
```

Отримати рядок з відновленим HTML.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає розібрану tidy-розмітку.

### Приклади

**Приклад #1 Приклад використання** tidy\_get\_output()\*\*\*\*

```php
<?php

$html = '<p>параграф</i>';
$tidy = tidy_parse_string($html);

$tidy->cleanRepair();

echo tidy_get_output($tidy);
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
<p>параграф</p>
</body>
</html>
```
