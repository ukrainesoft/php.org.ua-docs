---
navigation:
  - function.ob-tidyhandler.html: « obtidyhandler
  - function.tidy-config-count.html: tidyconfigcount »
  - index.html: PHP Manual
  - ref.tidy.html: Tidy
title: tidyaccesscount
---
# tidyaccesscount

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidyaccesscount — Повертає кількість доступних попереджень Tidy, які зустрілися у розглянутому документі

### Опис

```methodsynopsis
tidy_access_count(tidy $tidy): int
```

**tidyaccesscount()** повертає кількість доступних попереджень, знайдених у розглянутому документі.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Повертає кількість попереджень.

### Приклади

**Приклад #1 Приклад використання **tidyaccesscount()****

```php
<?php

$html ='<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html><head><title>Title</title></head>
<body>

<p><img src="img.png"></p>

</body></html>';


// выбирается уровень проверки доступности: 1, 2 или 3
$config = array('accessibility-check' => 3);

$tidy = new tidy();
$tidy->parseString($html, $config);
$tidy->cleanRepair();

/* Нельзя забывать про этот вызов! */
$tidy->diagnose();

echo tidy_access_count($tidy); //5

?>
```

### Примітки

> **Зауваження**
> 
> Відповідно до дизайну TidyLib, слід викликати [tidydiagnose()](tidy.diagnose.html) до **tidyaccesscount()** або останній завжди повертатиме `0`. Необхідно також вказувати параметр конфігурації `accessibility-check`

### Дивіться також

-   [tidyerrorcount()](function.tidy-error-count.html) - Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidywarningcount()](function.tidy-warning-count.html) - Повертає число Tidy-попереджень, зустрінутих у зазначеному документі
