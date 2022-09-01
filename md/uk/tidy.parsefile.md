---
navigation:
  - tidy.isxml.html: '« tidy::isXml'
  - tidy.parsestring.html: 'tidy::parseString »'
  - index.html: PHP Manual
  - class.tidy.html: tidy
title: 'tidy::parseFile'
---
# tidy::parseFile

# tidyparsefile

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::parseFile -- tidyparsefile — Розбір розмітки у файлі або URI

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

Якщо отримано параметр `filename`, то функція прочитає цей файл та ініціалізує об'єкт із цим файлом, так само як робить цю функцію **tidyparsefile()**

`config`

Налаштування `config` можуть бути задані у вигляді масиву чи рядка. Якщо заданий рядок, він інтерпретується як ім'я файлу конфігурації, інакше, параметр інтерпретується як самі настройки.

Інформацію про кожен параметр можна знайти тут: [» http://api.html-tidy.org/#quick-reference](http://api.html-tidy.org/#quick-reference)

`encoding`

Параметр `encoding` встановлює кодування для вхідних/вихідних документів. Можливі значення: `ascii` `latin0` `latin1` `raw` `utf8` `iso2022` `mac` `win1252` `ibm858` `utf16` `utf16le` `utf16be` `big5`, і `shiftjis`

`useIncludePath`

Пошук файлу в [includepath](ini.core.html#ini.include-path)

### Значення, що повертаються

**tidy::parseFile()** повертає **`true`** у разі успішного виконання . **tidyparsefile()** повертає новий екземпляр [tidy](class.tidy.html) у разі успішного виконання. І метод, і функція повертають **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `config` і `encoding` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **tidy::parseFile()****

```php
<?php
$tidy = new tidy();
$tidy->parseFile('file.html');

$tidy->cleanRepair();

if(!empty($tidy->errorBuffer)) {
    echo "Возникли следующие ошибки или предупреждения:\n";
    echo $tidy->errorBuffer;
}
?>
```

### Дивіться також

-   [tidy::parsestring()](tidy.parsestring.html) - Розбір документа, що зберігається у рядку
-   [tidy::repairfile()](tidy.repairfile.html) - Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairstring()](tidy.repairstring.html) - Відновлює рядок, використовуючи наскільки можна конфігураційний файл
