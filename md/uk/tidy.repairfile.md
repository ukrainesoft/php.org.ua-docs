---
navigation:
  - tidy.parsestring.md: '« tidy::parseString'
  - tidy.repairstring.md: 'tidy::repairString »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::repairFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::repairFile

# tidy\_repair\_file

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.7.0)

tidy::repairFile -- tidy\_repair\_file — Відновлює розмітку файлу та повертає його у вигляді рядка

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

Інформацію про кожен параметр можна знайти тут: [http://tidy.sourceforge.net/docs/quickref.md](http://tidy.sourceforge.net/docs/quickref.md)

`encoding`

Параметр`encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, и`shiftjis`

`useIncludePath`

Поиск файла в[include\_path](ini.core.md#ini.include-path)

### Значення, що повертаються

Повертає відновлений документ у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **tidy::repairFile()** тепер статичний метод. |
| 8.0.0 | `config`и`encoding` тепер допускають значення null. |

### Приклади

**Пример #1 Пример использования**tidy::repairFile()\*\*\*\*

```php
<?php
$file = 'file.md';

$tidy = new tidy();
$repaired = $tidy->repairfile($file);
rename($file, $file . '.bak');

file_put_contents($file, $repaired);
?>
```

### Дивіться також

-   [tidy::parseFile()](tidy.parsefile.md) \- Розбір розмітки у файлі або URI
-   [tidy::parseString()](tidy.parsestring.md) \- Розбір документа, що зберігається у рядку
-   [tidy::repairString()](tidy.repairstring.md) \- Відновлює рядок, використовуючи наскільки можна конфігураційний файл
