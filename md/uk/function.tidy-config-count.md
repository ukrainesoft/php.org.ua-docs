---
navigation:
  - function.tidy-access-count.md: « tidyaccesscount
  - function.tidy-error-count.md: tidyerrorcount »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidyconfigcount
---
# tidyconfigcount

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidyconfigcount — Повертає кількість помилок конфігурації Tidy, які зустрілися під час розгляду документа

### Опис

```methodsynopsis
tidy_config_count(tidy $tidy): int
```

Повертає кількість помилок у конфігурації заданого об'єкта `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає кількість помилок.

### Приклади

**Приклад #1 Приклад використання **tidyconfigcount()****

```php
<?php
$html = '<p>test</I>';

$config = array('doctype' => 'bogus');

$tidy = tidy_parse_string($html, $config);

/* Выведет 1, потому как 'bogus' некорректное объявление типа документа */
echo tidy_config_count($tidy);
?>
```
