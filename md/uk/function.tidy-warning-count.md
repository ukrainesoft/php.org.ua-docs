Повертає число Tidy-попереджень, зустрінутих у зазначеному документі

-   [« tidygetoutput](function.tidy-get-output.html)
    
-   [Лексер (Tokenizer) »](book.tokenizer.html)
    
-   [PHP Manual](index.html)
    
-   [Tidy](ref.tidy.html)
    
-   Повертає число Tidy-попереджень, зустрінутих у зазначеному документі
    

# tidywarningcount

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidywarningcount - Повертає число Tidy-попереджень, зустрінутих у зазначеному документі

### Опис

```methodsynopsis
tidy_warning_count(tidy $tidy): int
```

Повертає число Tidy-попереджень, що зустрічаються у зазначеному документі.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Повертає кількість попереджень.

### Приклади

**Приклад #1 Приклад використання **tidywarningcount()****

```php
<?php
$html = '<p>тест</i>
<bogustag>фикция</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1
echo tidy_warning_count($tidy) . "\n"; //5
?>
```

### Дивіться також

-   [tidyerrorcount()](function.tidy-error-count.html) - Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidyaccesscount()](function.tidy-access-count.html) - Повертає кількість доступних попереджень Tidy, що зустрілися у розглянутому документі