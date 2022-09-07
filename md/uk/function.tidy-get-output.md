---
navigation:
  - function.tidy-error-count.md: « tidyerrorcount
  - function.tidy-warning-count.md: tidywarningcount »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidygetoutput
---
# tidygetoutput

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidygetoutput - Повертає рядок, що представляє розібрану tidy-розмітку

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

**Приклад #1 Приклад використання **tidygetoutput()****

```php
<?php

$html = '<p>параграф</i>';
$tidy = tidy_parse_string($html);

$tidy->cleanRepair();

echo tidy_get_output($tidy);
?>
```

Результат виконання цього прикладу:

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
