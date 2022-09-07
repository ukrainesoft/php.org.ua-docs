---
navigation:
  - class.splfileobject.md: « SplFileObject
  - splfileobject.current.md: 'SplFileObject::current »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::construct'
---
# SplFileObject::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::construct — Створює об'єкт SplFileObject

### Опис

public **SplFileObject::construct**  
string `$filename`  
string `$mode` = "r",  
bool `$useIncludePath` **`false`**  
?resource `$context` **`null`**

Створює новий файловий об'єкт.

### Список параметрів

`filename`

Файл, який потрібно прочитати.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

`mode`

Режим роботи із файлом. Список можливих режимів роботи наведено в описі функції [fopen()](function.fopen.md)

`useIncludePath`

Чи потрібно переглядати [includepath](ini.core.md#ini.include-path) під час пошуку файлу `filename`

`context`

Допустимий ресурс контексту, створений функцією [streamcontextcreate()](function.stream-context-create.md)

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо файл `filename` неможливо відкрити.

Викидає виняток [LogicException](class.logicexception.md), якщо `filename` є каталогом.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::construct()****

Цей приклад відкриває поточний файл і перебирає його рядків.

```php
<?php
$file = new SplFileObject(__FILE__);
foreach ($file as $line_num => $line) {
    echo "Строка $line_num: $line";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Строка 0: <?php
Строка 1: $file = new SplFileObject(__FILE__);
Строка 2: foreach ($file as $line_num => $line) {
Строка 3:     echo "Line $line_num is $line";
Строка 4: }
Строка 5: ?>
```

### Дивіться також

-   [SplFileInfo::openFile()](splfileinfo.openfile.md) - Отримує об'єкт SplFileObject для файлу
-   [fopen()](function.fopen.md) - Відкриває файл або URL
