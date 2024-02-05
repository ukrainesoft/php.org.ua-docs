---
navigation:
  - tidy.repairfile.md: '« tidy::repairFile'
  - tidy.root.md: 'tidy::root »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::repairString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::repairString

# tidy\_repair\_string

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.7.0)

tidy::repairString -- tidy\_repair\_string — Відновлює рядок, використовуючи наскільки можна конфігураційний файл

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

Інформацію про кожен параметр можна знайти тут: [» http://api.md-tidy.org/#quick-reference](http://api.md-tidy.org/#quick-reference)

`encoding`

Параметр`encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, и`shiftjis`

### Значення, що повертаються

Повертає відновлений рядок або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **tidy::repairString()** тепер статичний метод. |
| 8.0.0 | `config`и`encoding` тепер допускають значення null. |
| 8.0.0 | Функція більше не приймає параметр `useIncludePath` |

### Приклади

**Пример #1 Пример использования**tidy::repairString()\*\*\*\*

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

$buffer = ob_get_clean();
$tidy = new tidy();
$clean = $tidy->repairString($buffer);

echo $clean;
?>
```

Результат виконання наведеного прикладу:

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

-   [tidy::parseFile()](tidy.parsefile.md) \- Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.md) \- Розбір документа, що зберігається у рядку
-   [tidy::repairFile()](tidy.repairfile.md) \- Відновлює розмітку файлу та повертає його у вигляді рядка
