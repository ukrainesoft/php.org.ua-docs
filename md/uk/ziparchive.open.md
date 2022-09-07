---
navigation:
  - ziparchive.locatename.md: '« ZipArchive::locateName'
  - ziparchive.registercancelcallback.md: 'ZipArchive::registerCancelCallback »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::open'
---
# ZipArchive::open

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::open — Відкриває ZIP-архів

### Опис

```methodsynopsis
public ZipArchive::open(string $filename, int $flags = 0): bool|int
```

Відкриває новий або існуючий ZIP-архів для читання, запису чи зміни.

Починаючи з libzip 1.6.0, порожній файл не є коректним архівом.

### Список параметрів

`filename`

Ім'я ZIP-архіву для відкриття.

`flags`

Режим відкриття файлів, що використовується.

-   **`[ZipArchive::OVERWRITE](zip.constants.md#ziparchive.constants.overwrite)`**
    
-   **`[ZipArchive::CREATE](zip.constants.md#ziparchive.constants.create)`**
    
-   **`[ZipArchive::RDONLY](zip.constants.md#ziparchive.constants.rdonly)`**
    
-   **`[ZipArchive::EXCL](zip.constants.md#ziparchive.constants.excl)`**
    
-   **`[ZipArchive::CHECKCONS](zip.constants.md#ziparchive.constants.checkcons)`**
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або один із наступних кодів помилки:

**`ZipArchive::ER_EXISTS`**

Файл існує.

**`ZipArchive::ER_INCONS`**

Несумісний ZIP-архів.

**`ZipArchive::ER_INVAL`**

Неприпустимий аргумент.

**`ZipArchive::ER_MEMORY`**

Помилка динамічного виділення пам'яті.

**`ZipArchive::ER_NOENT`**

Нема такого файлу.

**`ZipArchive::ER_NOZIP`**

Чи не є ZIP-архівом.

**`ZipArchive::ER_OPEN`**

Неможливо відкрити файл.

**`ZipArchive::ER_READ`**

Помилка читання.

**`ZipArchive::ER_SEEK`**

Помилка пошуку.

### Приклади

**Приклад #1 Відкриття та вилучення**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    echo 'готово';
    $zip->extractTo('test');
    $zip->close();
} else {
    echo 'ошибка с кодом:' . $res;
}
?>
```

**Приклад #2 Створення архіву**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('test.txt', 'содержимое файла');
    $zip->addFile('data.txt', 'entryname.txt');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

**Приклад #3 Створити архів**

```php
<?php
$name = tempnam(sys_get_temp_dir(), "FOO");
$zip = new ZipArchive;
$res = $zip->open($name, ZipArchive::OVERWRITE); /* усечение, поскольку пустой файл недопустим */
if ($res === TRUE) {
    $zip->addFile('data.txt', 'entryname.txt');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
