---
navigation:
  - tidy.isxml.md: '« tidy::isXml'
  - tidy.parsestring.md: 'tidy::parseString »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::parseFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::parseFile

# tidy\_parse\_file

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::parseFile -- tidy\_parse\_file — Розбір розмітки у файлі або URI

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::parseFile(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): bool
```

Процедурний стиль

```methodsynopsis
tidy_parse_file(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): tidy|false
```

Розбір одержаного файлу.

### Список параметрів

`filename`

Если получен параметр`filename`, то функція прочитає цей файл та ініціалізує об'єкт із цим файлом, так само як робить цю функцію **tidy\_parse\_file()**

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, він інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Інформацію про кожен параметр можна знайти тут: [» http://api.md-tidy.org/#quick-reference](http://api.md-tidy.org/#quick-reference)

`encoding`

Параметр`encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, и`shiftjis`

`useIncludePath`

Поиск файла в[include\_path](ini.core.md#ini.include-path)

### Значення, що повертаються

**tidy::parseFile()** повертає **`true`** у разі успішного виконання . **tidy\_parse\_file()** повертає новий екземпляр [tidy](class.tidy.md) у разі успішного виконання. І метод, і функція повертають \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `config`и`encoding` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання** tidy::parseFile()\*\*\*\*

```php
<?php
$tidy = new tidy();
$tidy->parseFile('file.md');

$tidy->cleanRepair();

if(!empty($tidy->errorBuffer)) {
    echo "Возникли следующие ошибки или предупреждения:\n";
    echo $tidy->errorBuffer;
}
?>
```

### Дивіться також

-   [tidy::parsestring()](tidy.parsestring.md) \- Розбір документа, що зберігається у рядку
-   [tidy::repairfile()](tidy.repairfile.md) \- Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairstring()](tidy.repairstring.md) \- Відновлює рядок, використовуючи наскільки можна конфігураційний файл
