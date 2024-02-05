---
navigation:
  - tidy.parsefile.md: '« tidy::parseFile'
  - tidy.repairfile.md: 'tidy::repairFile »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::parseString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::parseString

# tidy\_parse\_string

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::parseString -- tidy\_parse\_string — Розбір документа, що зберігається у рядку

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::parseString(string $string, array|string|null $config = null, ?string $encoding = null): bool
```

Процедурний стиль

```methodsynopsis
tidy_parse_string(string $string, array|string|null $config = null, ?string $encoding = null): tidy|false
```

Розбір документа, що зберігається у рядку.

### Список параметрів

`string`

Дані для аналізу.

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, він інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Інформацію про кожен параметр можна знайти тут: [» http://api.md-tidy.org/#quick-reference](http://api.md-tidy.org/#quick-reference)

`encoding`

Параметр`encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, и`shiftjis`

### Значення, що повертаються

**tidy::parseString()** повертає **`true`** у разі успішного виконання . **tidy\_parse\_string()** повертає новий екземпляр [tidy](class.tidy.md) у разі успішного виконання. І метод, і функція повертають \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `config`и`encoding` тепер допускають значення null. |

### Приклади

**Пример #1 Пример использования**tidy::parseString()\*\*\*\*

```php
<?php
ob_start();
?>

<html>
  <head>
   <title>тест</title>
  </head>
  <body>
   <p>ошибка<br>другая линия</i>
  </body>
</html>

<?php

$buffer = ob_get_clean();
$config = array('indent' => TRUE,
                'output-xhtml' => TRUE,
                'wrap' => 200);

$tidy = tidy_parse_string($buffer, $config, 'UTF8');

$tidy->cleanRepair();
echo $tidy;
?>
```

Результат виконання наведеного прикладу:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>
      тест
    </title>
  </head>
  <body>
    <p>
      ошибка<br />
      другая линия
    </p>
  </body>
</html>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.md) \- Розбір розмітки у файлі або URI
-   [tidy::repairFile()](tidy.repairfile.md) \- Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairString()](tidy.repairstring.md) \- Відновлює рядок, використовуючи наскільки можна конфігураційний файл
