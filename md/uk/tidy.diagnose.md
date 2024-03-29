---
navigation:
  - tidy.construct.md: '« tidy::\_\_construct'
  - tidy.props.errorbuffer.md: 'tidy::$errorBuffer »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::diagnose'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::diagnose

# tidy\_diagnose

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::diagnose -- tidy\_diagnose — Запуск настроєної діагностики для розібраної та відновленої розмітки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::diagnose(): bool
```

Процедурний стиль

```methodsynopsis
tidy_diagnose(tidy $tidy): bool
```

Виконує діагностичні тести отриманого об'єкту tidy `tidy`, додаючи деяку інформацію про документ у буфер помилок.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** tidy::diagnose()\*\*\*\*

```php
<?php

$html = <<< HTML
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<p>параграф</p>
HTML;

$tidy = tidy_parse_string($html);
$tidy->cleanRepair();

// обратите внимание на разницу между двумя выводами
echo $tidy->errorBuffer . "\n";

$tidy->diagnose();
echo $tidy->errorBuffer;

?>
```

Результат виконання наведеного прикладу:

```
line 4 column 1 - Warning: <p> isn't allowed in <head> elements
line 4 column 1 - Warning: inserting missing 'title' element
line 4 column 1 - Warning: <p> isn't allowed in <head> elements
line 4 column 1 - Warning: inserting missing 'title' element
Info: Doctype given is "-//W3C//DTD XHTML 1.0 Strict//EN"
Info: Document content looks like XHTML 1.0 Strict
2 warnings, 0 errors were found!
```

### Дивіться також

-   **tidy::errorBuffer()**
