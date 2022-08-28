Відновлює рядок, використовуючи наскільки можна конфігураційний файл

-   [« tidy::repairFile](tidy.repairfile.html)
    
-   [tidy::root »](tidy.root.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Відновлює рядок, використовуючи наскільки можна конфігураційний файл
    

# tidy::repairString

# tidyrepairstring

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.7.0)

tidy::repairString -- tidyrepairstring — Відновлює рядок за допомогою конфігураційного файлу.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static tidy::repairString(string $string, array|string|null $config = null, ?string $encoding = null): string|false
```

Процедурний стиль

```methodsynopsis
tidy_repair_string(string $string, array|string|null $config = null, ?string $encoding = null): string|false
```

Відновлює отриманий рядок.

### Список параметрів

`string`

Дані відновлення.

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, він інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Інформацію про кожен параметр можна знайти тут: [» http://api.html-tidy.org/#quick-reference](http://api.html-tidy.org/#quick-reference)

`encoding`

Параметр `encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, і `shiftjis`

### Значення, що повертаються

Повертає відновлений рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                              |
|--------|-------------------------------------------------------|
|        | **tidy::repairString()** тепер статичний метод.       |
|        | `config` і `encoding` тепер допускають значення null. |
|        | Функція більше не приймає параметр `useIncludePath`   |

### Приклади

**Приклад #1 Приклад використання **tidy::repairString()****

```php
<?php
ob_start();
?>

<html>
  <head>
    <title>тест</title>
  </head>
  <body>
    <p>ошибка</i>
  </body>
</html>

<?php

$buffer = ob_get_clean();
$tidy = new tidy();
$clean = $tidy->repairString($buffer);

echo $clean;
?>
```

Результат виконання цього прикладу:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html>
<head>
<title>тест</title>
</head>
<body>
<p>ошибка</p>
</body>
</html>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.html) - Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.html) - Розбір документа, що зберігається у рядку
-   [tidy::repairFile()](tidy.repairfile.html) - Відновлює розмітку файлу та повертає його у вигляді рядка