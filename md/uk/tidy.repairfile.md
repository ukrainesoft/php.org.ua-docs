Відновлює розмітку файлу та повертає його у вигляді рядка

-   [« tidy::parseString](tidy.parsestring.html)
    
-   [tidy::repairString »](tidy.repairstring.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Відновлює розмітку файлу та повертає його у вигляді рядка
    

# tidy::repairFile

# tidyrepairfile

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.7.0)

tidy::repairFile -- tidyrepairfile — Відновлює розмітку файлу та повертає його у вигляді рядка

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static tidy::repairFile(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): string|false
```

Процедурний стиль

```methodsynopsis
tidy_repair_file(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): string|false
```

Відновлює отриманий файл та повертає його у вигляді рядка.

### Список параметрів

`filename`

Ім'я файлу для відновлення.

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, він інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Інформацію про кожен параметр можна знайти тут: [http://tidy.sourceforge.net/docs/quickref.html](http://tidy.sourceforge.net/docs/quickref.html)

`encoding`

Параметр `encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, і `shiftjis`

`useIncludePath`

Пошук файлу в [include\_path](ini.core.html#ini.include-path)

### Значення, що повертаються

Повертає відновлений документ у вигляді рядка або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | **tidy::repairFile()** тепер статичний метод. |
|  | `config` і `encoding` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **tidy::repairFile()****

```php
<?php
$file = 'file.html';

$tidy = new tidy();
$repaired = $tidy->repairfile($file);
rename($file, $file . '.bak');

file_put_contents($file, $repaired);
?>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.html) - Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.html) - Розбір документа, що зберігається у рядку
-   [tidy::repairString()](tidy.repairstring.html) - Відновлює рядок, використовуючи наскільки можна конфігураційний файл