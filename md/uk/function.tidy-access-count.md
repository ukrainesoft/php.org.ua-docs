---
navigation:
  - function.ob-tidyhandler.md: « ob\_tidyhandler
  - function.tidy-config-count.md: tidy\_config\_count »
  - index.md: PHP Manual
  - ref.tidy.md: Tidy
title: tidy\_access\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy\_access\_count

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy\_access\_count — Повертає кількість доступних попереджень Tidy, які зустрілися у розглянутому документі

### Опис

```methodsynopsis
tidy_access_count(tidy $tidy): int
```

**tidy\_access\_count()** повертає кількість доступних попереджень, знайдених у розглянутому документі.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає кількість попереджень.

### Приклади

**Приклад #1 Приклад використання** tidy\_access\_count()\*\*\*\*

```php
<?php

$html ='<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html><head><title>Title</title></head>
<body>

<p><img src="img.png"></p>

</body></html>';


// выбирается уровень проверки доступности: 1, 2 или 3
$config = array('accessibility-check' => 3);

$tidy = new tidy();
$tidy->parseString($html, $config);
$tidy->cleanRepair();

/* Нельзя забывать про этот вызов! */
$tidy->diagnose();

echo tidy_access_count($tidy); //5

?>
```

### Примітки

> **Зауваження** :
> 
> Відповідно до дизайну TidyLib, слід викликати [tidy\_diagnose()](tidy.diagnose.md)до**tidy\_access\_count()** або останній завжди повертатиме . Необхідно також вказувати параметр конфігурації `accessibility-check`

### Дивіться також

-   [tidy\_error\_count()](function.tidy-error-count.md) \- Повертає кількість помилок Tidy, які зустрілися під час розгляду документа
-   [tidy\_warning\_count()](function.tidy-warning-count.md) \- Повертає число Tidy-попереджень, зустрінуті у зазначеному документі
