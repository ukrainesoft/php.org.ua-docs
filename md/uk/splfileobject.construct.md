---
navigation:
  - class.splfileobject.md: « SplFileObject
  - splfileobject.current.md: 'SplFileObject::current »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::\_\_construct — Створює об'єкт SplFileObject

### Опис

public **SplFileObject::\_\_construct**  
string`$filename`,  
string`$mode` = "r",  
bool`$useIncludePath` **`false`**,  
?resource`$context` **`null`**  
) .

Створює новий файловий об'єкт.

### Список параметрів

`filename`

Файл, який потрібно прочитати.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

`mode`

Режим роботи із файлом. Список можливих режимів роботи наведено в описі функції [fopen()](function.fopen.md)

`useIncludePath`

Чи потрібно переглядати [include\_path](ini.core.md#ini.include-path)во время поиска файла`filename`

`context`

Допустимий ресурс контексту, створений функцією [stream\_context\_create()](function.stream-context-create.md)

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо файл `filename` неможливо відкрити.

Викидає виняток [LogicException](class.logicexception.md), якщо `filename` є каталогом.

### Приклади

**Приклад #1 Приклад використання** SplFileObject::\_\_construct()\*\*\*\*

Цей приклад відкриває поточний файл і перебирає його рядків.

```php
<?php
$file = new SplFileObject(__FILE__);
foreach ($file as $line_num => $line) {
    echo "Строка $line_num: $line";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Строка 0: <?php
Строка 1: $file = new SplFileObject(__FILE__);
Строка 2: foreach ($file as $line_num => $line) {
Строка 3:     echo "Line $line_num is $line";
Строка 4: }
Строка 5: ?>
```

### Дивіться також

-   [SplFileInfo::openFile()](splfileinfo.openfile.md) \- Отримує об'єкт SplFileObject для файлу
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
