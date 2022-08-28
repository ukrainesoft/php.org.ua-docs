Створює новий tidy-об'єкт

-   [« tidy::cleanRepair](tidy.cleanrepair.html)
    
-   [tidy::diagnose »](tidy.diagnose.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Створює новий tidy-об'єкт
    

# tidy::construct

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::construct — Створює новий [tidy](class.tidy.html)об'єкт

### Опис

public **tidy::construct**  
?string `$filename` **`null`**  
array|string|null `$config` **`null`**  
?string `$encoding` **`null`**  
bool `$useIncludePath` **`false`**  

Створює новий [tidy](class.tidy.html)об'єкт.

### Список параметрів

`filename`

Якщо встановлено параметр `filename`, то ця функція прочитає файл та ініціалізує об'єкт із цим файлом, діючи як функція [tidy\_parse\_file()](tidy.parsefile.html)

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, це інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Опис кожного параметра можна знайти тут: [» http://api.html-tidy.org/#quick-reference](http://api.html-tidy.org/#quick-reference)

`encoding`

Параметр `encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, і `shiftjis`

`useIncludePath`

Пошук файлу в [include\_path](ini.core.html#ini.include-path)

### список змін

| Версия | Описание                                                                          |
|--------|-----------------------------------------------------------------------------------|
|        | `filename` `config` `encoding` і `useIncludePath` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **tidy::construct()****

```php
<?php

$html = <<< HTML

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head><title>title</title></head>
<body>
<p>параграф <bt />
текст</p>
</body></html>

HTML;

$tidy = new tidy();
$tidy->ParseString($html);

$tidy->cleanRepair();

if ($tidy->errorBuffer) {
    echo "Были обнаружены следующие ошибки:\n";
    echo $tidy->errorBuffer;
}

?>
```

Результат виконання цього прикладу:

```
Были обнаружены следующие ошибки:
line 8 column 14 - Error: <bt> is not recognized!
line 8 column 14 - Warning: discarding unexpected <bt>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.html) - Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.html) - Розбір документа, що зберігається у рядку