Отримує статус зазначеного документа

-   [« tidy::getRelease](tidy.getrelease.html)
    
-   [tidy::head »](tidy.head.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Отримує статус зазначеного документа
    

# tidy::getStatus

# tidygetstatus

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::getStatus -- tidygetstatus — Отримує статус зазначеного документа

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::getStatus(): int
```

Процедурний стиль

```methodsynopsis
tidy_get_status(tidy $tidy): int
```

Повертає статус вказаного tidy-об'єкта `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Повертає 0, якщо не було помилок/попереджень, 1 – для попереджень або можливих помилок або 2 – для помилок.

### Приклади

**Приклад #1 Приклад використання **tidy::getStatus()****

```php
<?php
$html = '<p>параграф</i>';
$tidy = new tidy();
$tidy->parseString($html);

$tidy2 = new tidy();
$html2 = '<bogus>тест</bogus>';
$tidy2->parseString($html2);

echo $tidy->getStatus(); //1

echo $tidy2->getStatus(); //2
?>
```