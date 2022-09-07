---
navigation:
  - tidy.getopt.md: '« tidy::getOpt'
  - tidy.getrelease.md: 'tidy::getRelease »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::getOptDoc'
---
# tidy::getOptDoc

# tidygetoptdoc

(PHP 5> = 5.1.0, PHP 7, PHP 8)

tidy::getOptDoc -- tidygetoptdoc — Повертає опис для опції із зазначеною назвою

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::getOptDoc(string $option): string|false
```

Процедурний стиль

```methodsynopsis
tidy_get_opt_doc(tidy $tidy, string $option): string|false
```

Функція **tidygetoptdoc()** повертає опис для опції із зазначеною назвою.

> **Зауваження**
> 
> Для використання цієї функції вам знадобиться бібліотека libtidy мінімум від 25 квітня 2005 року.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

`optname`

Назва опції

### Значення, що повертаються

Повертається рядок існуючої опції та наявний опис, інакше повертається **`false`**

### Приклади

**Приклад #1 Друк усіх опцій разом із описом та значенням за замовчуванням**

```php
<?php

$tidy = new tidy;
$config = $tidy->getConfig();

ksort($config);

foreach ($config as $opt => $val) {

    if (!$doc = $tidy->getOptDoc($opt))
        $doc = 'документация не существует!';

    $val = ($tidy->getOpt($opt) === true)  ? 'true'  : $val;
    $val = ($tidy->getOpt($opt) === false) ? 'false' : $val;

    echo "<p><b>$opt</b> (default: '$val')<br />".
         "$doc</p><hr />\n";
}

?>
```

### Дивіться також

-   [tidy::getconfig()](tidy.getconfig.md) - Отримує поточну конфігурацію Tidy
-   [tidy::getopt()](tidy.getopt.md) - Повертає значення вказаного параметра конфігурації для документа tidy
