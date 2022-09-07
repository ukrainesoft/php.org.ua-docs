---
navigation:
  - tidy.gethtmlver.md: '« tidy::getHtmlVer'
  - tidy.getoptdoc.md: 'tidy::getOptDoc »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::getOpt'
---
# tidy::getOpt

# tidygetopt

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::getOpt -- tidygetopt — Повертає значення вказаного параметра конфігурації для документа tidy

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::getOpt(string $option): string|int|bool
```

Процедурний стиль

```methodsynopsis
tidy_getopt(tidy $tidy, string $option): string|int|bool
```

Повертає значення вказаного параметра `option` для вказаного об'єкту tidy `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

`option`

Ви можете знайти список кожної опції конфігурації з типом тут: [» http://api.html-tidy.org/#quick-reference](http://api.html-tidy.org/#quick-reference)

### Значення, що повертаються

Повертає значення вказаної опції `option`. Тип значення, що повертається, залежить від типу зазначеної опції.

### Приклади

**Приклад #1 Приклад використання **tidygetopt()****

```php
<?php

$html ='<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html><head><title>Заголовок</title></head>
<body>

<p><img src="img.png"></p>

</body></html>';

$config = array('accessibility-check' => 3,
                'alt-text' => 'какой-то текст');

$tidy = new tidy();
$tidy->parseString($html, $config);


var_dump($tidy->getOpt('accessibility-check')); //integer
var_dump($tidy->getOpt('lower-literals')); //boolean
var_dump($tidy->getOpt('alt-text')); //string

?>
```

Результат виконання цього прикладу:

```
int(3)
bool(true)
string(9) "какой-то текст"
```
