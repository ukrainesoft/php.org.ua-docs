---
navigation:
  - function.tidy-config-count.md: « tidy\_config\_count
  - function.tidy-get-output.md: tidy\_get\_output »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidy\_error\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy\_error\_count

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy\_error\_count — Повертає кількість помилок Tidy, які зустрілися під час розгляду документа

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

**Приклад #1 Приклад використання** tidy\_error\_count()\*\*\*\*

```php
<?php
$html = '<p>test</i>
<bogustag>bogus</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1

echo $tidy->errorBuffer;
?>
```

Результат виконання наведеного прикладу:

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

-   [tidy\_access\_count()](function.tidy-access-count.md) \- Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
-   [tidy\_warning\_count()](function.tidy-warning-count.md) \- Повертає число Tidy-попереджень, зустрінуті у зазначеному документі
