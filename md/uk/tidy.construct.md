---
navigation:
  - tidy.cleanrepair.md: '« tidy::cleanRepair'
  - tidy.diagnose.md: 'tidy::diagnose »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::\_\_construct

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::\_\_construct — Створює новий [tidy](class.tidy.md)\-об'єкт

### Опис

public**tidy::\_\_construct**  
?string`$filename` **`null`**,  
array|string|null`$config` **`null`**,  
?string`$encoding` **`null`**,  
bool`$useIncludePath` **`false`**  
) .

Створює новий [tidy](class.tidy.md)\-об'єкт.

### Список параметрів

`filename`

Если задан параметр`filename`, то ця функція прочитає файл та ініціалізує об'єкт із цим файлом, діючи як функція [tidy\_parse\_file()](tidy.parsefile.md)

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, це інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Опис каждого параметра можно найти тут:[» http://api.md-tidy.org/#quick-reference](http://api.md-tidy.org/#quick-reference)

`encoding`

Параметр`encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, и`shiftjis`

`useIncludePath`

Поиск файла в[include\_path](ini.core.md#ini.include-path)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `filename` `config` `encoding`и`useIncludePath` тепер допускають значення null. |

### Приклади

**Пример #1 Пример использования**tidy::\_\_construct()\*\*\*\*

```php
<?php

$html = <<< HTML

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head><title>title</title></head>
<body>
<p>параграф <bt />
текст</p>
</body></html>

HTML;

$tidy = new tidy();
$tidy->ParseString($html);

$tidy->cleanRepair();

if ($tidy->errorBuffer) {
    echo "Были обнаружены следующие ошибки:\n";
    echo $tidy->errorBuffer;
}

?>
```

Результат виконання наведеного прикладу:

```
Были обнаружены следующие ошибки:
line 8 column 14 - Error: <bt> is not recognized!
line 8 column 14 - Warning: discarding unexpected <bt>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.md) \- Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.md) \- Розбір документа, що зберігається у рядку
