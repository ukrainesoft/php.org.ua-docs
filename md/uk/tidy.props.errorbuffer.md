Повертає попередження та помилки, що виникли при розборі зазначеного документа

-   [« tidy::diagnose](tidy.diagnose.html)
    
-   [tidy::getConfig »](tidy.getconfig.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Повертає попередження та помилки, що виникли при розборі зазначеного документа
    

# tidy::$errorBuffer

# tidygeterrorbuffer

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::$errorBuffer -- tidygeterrorbuffer — Повертає попередження та помилки, що виникли під час аналізу зазначеного документа

### Опис

Об'єктно-орієнтований стиль (property):

public string [$tidy->errorBuffer](tidy.props.errorbuffer.html)

Процедурний стиль:

```methodsynopsis
tidy_get_error_buffer(tidy $tidy): string|false
```

Повертає попередження та помилки, що виникли при розборі зазначеного документа.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

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

-   [tidyaccesscount()](function.tidy-access-count.html) - Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі
-   [tidyerrorcount()](function.tidy-error-count.html) - Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidywarningcount()](function.tidy-warning-count.html) - Повертає число Tidy-попереджень, зустрінуті у зазначеному документі