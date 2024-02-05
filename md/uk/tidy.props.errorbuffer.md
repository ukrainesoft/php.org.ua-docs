---
navigation:
  - tidy.diagnose.md: '« tidy::diagnose'
  - tidy.getconfig.md: 'tidy::getConfig »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::$errorBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::$errorBuffer

# tidy\_get\_error\_buffer

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::$errorBuffer -- tidy\_get\_error\_buffer — Повертає попередження та помилки, що виникли під час аналізу зазначеного документа

### Опис

Об'єктно-орієнтований стиль (property):

public string[$tidy->errorBuffer](tidy.props.errorbuffer.md)

Процедурний стиль:

```methodsynopsis
tidy_get_error_buffer(tidy $tidy): string|false
```

Повертає попередження та помилки, що виникли при розборі зазначеного документа.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає буфер помилки у вигляді рядка або \*\*`false`\*\*якщо буфер порожній.

### Приклади

**Приклад #1 Приклад використання** tidy\_get\_error\_buffer()\*\*\*\*

```php
<?php
$html = '<p>параграф</p>';

$tidy = tidy_parse_string($html);

echo tidy_get_error_buffer($tidy);
/* или в ООП стиле: */
echo $tidy->errorBuffer;
?>
```

Результат виконання наведеного прикладу:

```
line 1 column 1 - Warning: missing <!DOCTYPE> declaration
line 1 column 1 - Warning: inserting missing 'title' element
```

### Дивіться також

-   [tidy\_access\_count()](function.tidy-access-count.md) \- Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
-   [tidy\_error\_count()](function.tidy-error-count.md) \- Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidy\_warning\_count()](function.tidy-warning-count.md) \- Повертає число Tidy-попереджень, зустрінуті у зазначеному документі
