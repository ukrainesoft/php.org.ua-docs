---
navigation:
  - function.file-get-contents.md: « file\_get\_contents
  - function.file.md: file »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: file\_put\_contents
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# file\_put\_contents

(PHP 5, PHP 7, PHP 8)

file\_put\_contents — Пише дані у файл

### Опис

```methodsynopsis
file_put_contents(    string $filename,    mixed $data,    int $flags = 0,    ?resource $context = null): int|false
```

Функція ідентична послідовним успішним викликам функцій [fopen()](function.fopen.md) [fwrite()](function.fwrite.md) і [fclose()](function.fclose.md)

Якщо `filename` немає, файл буде створено. Інакше існуючий файл буде перезаписано, за винятком випадку, якщо вказано прапор **`FILE_APPEND`**

### Список параметрів

`filename`

Шлях до файлу, що записується.

`data`

Дані, що записуються. Може бути типу string, array або ресурсом потоку.

Якщо `data` є потоковим ресурсом (stream), буфер цього потоку, що залишився, буде скопійований у зазначений файл. Це схоже на використання функції [stream\_copy\_to\_stream()](function.stream-copy-to-stream.md)

Також ви можете передати одновимірний масив як параметр `data`. Це буде еквівалентно виклику `file_put_contents($filename, implode('', $array))`

`flags`

Значением параметра`flags` може бути будь-яка комбінація наступних прапорів, з'єднаних бінарним оператором АБО (

**Доступні прапори**

| Флаг | Опис |
| --- | --- |
| **`FILE_USE_INCLUDE_PATH`** | Шукає `filename` в директоріях, що підключаються. Детальніше дивіться директиву [include\_path](ini.core.md#ini.include-path) |
| **`FILE_APPEND`** | Якщо файл `filename` вже існує, дані будуть дописані в кінець файлу замість його перезаписати. |
| **`LOCK_EX`** | Отримати ексклюзивне блокування файлу під час запису. Іншими словами, між викликами [fopen()](function.fopen.md) і [fwrite()](function.fwrite.md) відбудеться виклик функції [flock()](function.flock.md). . Це не одне й те саме, що виклик [fopen()](function.fopen.md) з прапором "х". |

`context`

Коректний ресурс контексту, створений за допомогою функції [stream\_context\_create()](function.stream-context-create.md)

### Значення, що повертаються

Функція повертає кількість записаних байт у файл, або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад простого використання**

```php
<?php
$file = 'people.txt';
// Открываем файл для получения существующего содержимого
$current = file_get_contents($file);
// Добавляем нового человека в файл
$current .= "John Smith\n";
// Пишем содержимое обратно в файл
file_put_contents($file, $current);
?>
```

**Приклад #2 Використання прапорів**

```php
<?php
$file = 'people.txt';
// Новый человек, которого нужно добавить в файл
$person = "John Smith\n";
// Пишем содержимое в файл,
// используя флаг FILE_APPEND для дописывания содержимого в конец файла
// и флаг LOCK_EX для предотвращения записи данного файла кем-нибудь другим в данное время
file_put_contents($file, $person, FILE_APPEND | LOCK_EX);
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Дивіться також

-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
-   [file\_get\_contents()](function.file-get-contents.md) \- Читає вміст файлу в рядок
-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
