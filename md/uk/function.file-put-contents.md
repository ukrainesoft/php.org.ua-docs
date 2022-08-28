Пише дані у файл

-   [« file\_get\_contents](function.file-get-contents.html)
    
-   [file »](function.file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Пише дані у файл
    

# fileputcontents

(PHP 5, PHP 7, PHP 8)

fileputcontents — Пише дані у файл

### Опис

```methodsynopsis
file_put_contents(    string $filename,    mixed $data,    int $flags = 0,    ?resource $context = null): int|false
```

Функція ідентична послідовним успішним викликам функцій [fopen()](function.fopen.html) [fwrite()](function.fwrite.html) і [fclose()](function.fclose.html)

Якщо `filename` немає, файл буде створено. Інакше існуючий файл буде перезаписано, за винятком випадку, якщо вказано прапор **`FILE_APPEND`**

### Список параметрів

`filename`

Шлях до файлу, що записується.

`data`

Дані, що записуються. Може бути типу string, array або ресурсом потоку.

Якщо `data` є потоковим ресурсом (stream), буфер цього потоку, що залишився, буде скопійований у зазначений файл. Це схоже на використання функції [stream\_copy\_to\_stream()](function.stream-copy-to-stream.html)

Також ви можете передати одновимірний масив як параметр `data`. Це буде еквівалентно виклику `file_put_contents($filename, implode('', $array))`

`flags`

Значення параметра `flags` може бути будь-яка комбінація наступних прапорів, з'єднаних бінарним оператором АБО (`|`

**Доступні прапори**

| Флаг | Описание |
| --- | --- |
| **`FILE_USE_INCLUDE_PATH`** | Шукає `filename` в директоріях, що підключаються. Детальніше дивіться директиву [include\_path](ini.core.html#ini.include-path) |
| **`FILE_APPEND`** | Якщо файл `filename` вже існує, дані будуть дописані в кінець файлу замість його перезаписати. |
| **`LOCK_EX`** | Отримати ексклюзивне блокування файлу під час запису. Іншими словами, між викликами [fopen()](function.fopen.html) і [fwrite()](function.fwrite.html) відбудеться виклик функції [flock()](function.flock.html). Це не одне й те саме, що виклик [fopen()](function.fopen.html) з прапором "х". |

`context`

Коректний ресурс контексту, створений за допомогою функції [stream\_context\_create()](function.stream-context-create.html)

### Значення, що повертаються

Функція повертає кількість записаних байт у файл, або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення **`false`**так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад простого використання**

```php
<?php
$file = 'people.txt';
// Открываем файл для получения существующего содержимого
$current = file_get_contents($file);
// Добавляем нового человека в файл
$current .= "John Smith\n";
// Пишем содержимое обратно в файл
file_put_contents($file, $current);
?>
```

**Приклад #2 Використання прапорів**

```php
<?php
$file = 'people.txt';
// Новый человек, которого нужно добавить в файл
$person = "John Smith\n";
// Пишем содержимое в файл,
// используя флаг FILE_APPEND для дописывания содержимого в конец файла
// и флаг LOCK_EX для предотвращения записи данного файла кем-нибудь другим в данное время
file_put_contents($file, $person, FILE_APPEND | LOCK_EX);
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.html). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Поддерживаемые протоколы и обёртки](wrappers.html)

### Дивіться також

-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [fwrite()](function.fwrite.html) - Бінарно-безпечний запис у файл
-   [file\_get\_contents()](function.file-get-contents.html) - Читає вміст файлу в рядок
-   [stream\_context\_create()](function.stream-context-create.html) - Створює контекст потоку