---
navigation:
  - bzip2.constants.md: « Обумовлені константи
  - ref.bzip2.md: Функції Bzip2 »
  - index.md: PHP Manual
  - book.bzip2.md: Bzip2
title: Приклади
---
# Приклади

Наступний приклад відкриє тимчасовий файл, запише до нього тестовий рядок, після чого виведе вміст файлу.

**Приклад #1 Приклад роботи з bzip2**

```php
<?php

$filename = "/tmp/testfile.bz2";
$str = "This is a test string.\n";

// открываем файл для записи
$bz = bzopen($filename, "w");

// пишем строку в файл
bzwrite($bz, $str);

// закрываем файл
bzclose($bz);

// открываем файл для чтения
$bz = bzopen($filename, "r");

// читаем 10 символов
echo bzread($bz, 10);

// выводим всё, до конца файла (или следующие 1024 символа) и закрываем его.
echo bzread($bz);

bzclose($bz);

?>
```
