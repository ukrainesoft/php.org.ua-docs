---
navigation:
  - function.tidy-config-count.html: « tidyconfigcount
  - function.tidy-get-output.html: tidygetoutput »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidyerrorcount
---
# tidyerrorcount

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidyerrorcount — Повертає кількість помилок Tidy, які зустрілися під час розгляду документа

### Опис

```methodsynopsis
tidy_error_count(tidy $tidy): int
```

Повертає кількість помилок Tidy, що зустрілися під час розгляду документа.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає кількість помилок Tidy.

### Приклади

**Приклад #1 Приклад використання **tidyerrorcount()****

```php
<?php
$html = '<p>test</i>
<bogustag>bogus</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1

echo $tidy->errorBuffer;
?>
```

Результат виконання цього прикладу:

```
1
line 1 column 1 - Warning: missing <!DOCTYPE> declaration
line 1 column 8 - Warning: discarding unexpected </i>
line 2 column 1 - Error: <bogustag> is not recognized!
line 2 column 1 - Warning: discarding unexpected <bogustag>
line 2 column 16 - Warning: discarding unexpected </bogustag>
line 1 column 1 - Warning: inserting missing 'title' element
```

### Дивіться також

-   [tidyaccesscount()](function.tidy-access-count.html) - Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
-   [tidywarningcount()](function.tidy-warning-count.html) - Повертає число Tidy-попереджень, зустрінутих у зазначеному документі
