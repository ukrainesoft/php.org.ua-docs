---
navigation:
  - function.pclose.md: « pclose
  - function.readfile.md: readfile »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: popen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# popen

(PHP 4, PHP 5, PHP 7, PHP 8)

popen — Відкриває файловий покажчик процесу

### Опис

```methodsynopsis
popen(string $command, string $mode): resource|false
```

Відкриває потік до процесу, що виконується за допомогою форки команди, заданої в параметрі `command`

### Список параметрів

`command`

Команда

`mode`

Режим. Либо`'r'`для чтения, либо`'w'`для записи.

В Windows для**popen()** за умовчанням використовується текстовий режим, тобто. будь-які символи `\n`, записані в канал або прочитані з нього, будуть перетворені на `\r\n`. Якщо це небажано, можна примусово використовувати бінарний режим, встановивши для `mode`значение`'rb'`и`'wb'`соответственно.

### Значення, що повертаються

Повертає файловий покажчик, ідентичний функцією, що повертається. [fopen()](function.fopen.md), за винятком того, що він односторонній (може бути використаний тільки для читання або запису) і повинен бути закритий за допомогою [pclose()](function.pclose.md). Цей покажчик може бути використаний з [fgets()](function.fgets.md) [fgetss()](function.fgetss.md) і [fwrite()](function.fwrite.md). . Якщо в якості режиму вказано 'r', файловий покажчик аналогічний потоку виводу (STDOUT) команди, а якщо вказано 'w', то файловий покажчик аналогічний потоку введення (STDIN) команди.

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання функції** popen()\*\*\*\*

```php
<?php
$handle = popen("/bin/ls", "r");
?>
```

Якщо команда для виконання не знайдено, буде повернено коректний ресурс. Це може мати дивний вигляд, але має сенс; це дає можливість отримати доступ до будь-якого повідомлення про помилку, яке поверне оболонка:

**Приклад #2 Приклад використання функції** popen()\*\*\*\*

```php
<?php
error_reporting(E_ALL);

/* Добавляем перенаправление, чтобы прочитать stderr. */
$handle = popen('/path/to/executable 2>&1', 'r');
echo "'$handle'; " . gettype($handle) . "\n";
$read = fread($handle, 2096);
echo $read;
pclose($handle);
?>
```

### Примітки

> **Зауваження** :
> 
> Якщо вам потрібна двостороння передача (обидві сторони одночасно), використовуйте [proc\_open()](function.proc-open.md)

### Дивіться також

-   [pclose()](function.pclose.md) \- Закриває файловий покажчик процесу
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [proc\_open()](function.proc-open.md) \- Виконати команду та відкрити покажчик на файл для введення/виводу
