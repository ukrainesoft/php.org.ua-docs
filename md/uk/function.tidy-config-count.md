---
navigation:
  - function.tidy-access-count.md: « tidy\_access\_count
  - function.tidy-error-count.md: tidy\_error\_count »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidy\_config\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy\_config\_count

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy\_config\_count — Повертає кількість помилок конфігурації Tidy, які зустрілися під час розгляду документа

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

**Пример #1 Пример использования**tidy\_config\_count()\*\*\*\*

```php
<?php
$html = '<p>test</I>';

$config = array('doctype' => 'bogus');

$tidy = tidy_parse_string($html, $config);

/* Выведет 1, потому как 'bogus' некорректное объявление типа документа */
echo tidy_config_count($tidy);
?>
```
