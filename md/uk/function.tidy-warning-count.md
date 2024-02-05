---
navigation:
  - function.tidy-get-output.md: « tidy\_get\_output
  - book.tokenizer.md: Лексер (Tokenizer) »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidy\_warning\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy\_warning\_count

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy\_warning\_count - Повертає число Tidy-попереджень, зустрінутих у зазначеному документі

### Опис

```methodsynopsis
tidy_warning_count(tidy $tidy): int
```

Повертає число Tidy-попереджень, що зустрічаються у зазначеному документі.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає кількість попереджень.

### Приклади

**Пример #1 Пример использования**tidy\_warning\_count()\*\*\*\*

```php
<?php
$html = '<p>тест</i>
<bogustag>фикция</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1
echo tidy_warning_count($tidy) . "\n"; //5
?>
```

### Дивіться також

-   [tidy\_error\_count()](function.tidy-error-count.md) \- Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidy\_access\_count()](function.tidy-access-count.md) \- Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
