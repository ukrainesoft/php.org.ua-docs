---
navigation:
  - tidy.diagnose.md: '« tidy::diagnose'
  - tidy.getconfig.md: 'tidy::getConfig »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::$errorBuffer'
---
# tidy::$errorBuffer

# tidygeterrorbuffer

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::$errorBuffer -- tidygeterrorbuffer — Повертає попередження та помилки, що виникли під час аналізу зазначеного документа

### Опис

Об'єктно-орієнтований стиль (property):

public string [$tidy->errorBuffer](tidy.props.errorbuffer.md)

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

**Приклад #1 Приклад використання **tidygeterrorbuffer()****

```php
<?php
$html = '<p>параграф</p>';

$tidy = tidy_parse_string($html);

echo tidy_get_error_buffer($tidy);
/* или в ООП стиле: */
echo $tidy->errorBuffer;
?>
```

Результат виконання цього прикладу:

```
line 1 column 1 - Warning: missing <!DOCTYPE> declaration
line 1 column 1 - Warning: inserting missing 'title' element
```

### Дивіться також

-   [tidyaccesscount()](function.tidy-access-count.md) - Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
-   [tidyerrorcount()](function.tidy-error-count.md) - Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidywarningcount()](function.tidy-warning-count.md) - Повертає число Tidy-попереджень, зустрінуті у зазначеному документі
