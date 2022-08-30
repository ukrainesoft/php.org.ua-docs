Створює об'єкт SplFileObject

-   [« SplFileObject](class.splfileobject.html)
    
-   [SplFileObject::current »](splfileobject.current.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Створює об'єкт SplFileObject
    

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

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.html). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.html)

`mode`

Режим роботи із файлом. Список можливих режимів роботи наведено в описі функції [fopen()](function.fopen.html)

`useIncludePath`

Чи потрібно переглядати [includepath](ini.core.html#ini.include-path) під час пошуку файлу `filename`

`context`

Допустимий ресурс контексту, створений функцією [streamcontextcreate()](function.stream-context-create.html)

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо файл `filename` неможливо відкрити.

Викидає виняток [LogicException](class.logicexception.html), якщо `filename` є каталогом.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::construct()****

Цей приклад відкриває поточний файл і перебирає його рядків.

```php
<?php
$file = new SplFileObject(__FILE__);
foreach ($file as $line_num => $line) {
    echo "Строка $line_num: $line";
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

-   [SplFileInfo::openFile()](splfileinfo.openfile.html) - Отримує об'єкт SplFileObject для файлу
-   [fopen()](function.fopen.html) - Відкриває файл або URL