---
navigation:
  - splfileobject.flock.md: '« SplFileObject::flock'
  - splfileobject.fputcsv.md: 'SplFileObject::fputcsv »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fpassthru'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fpassthru

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fpassthru — Виводить весь вміст файлу, що залишився, у вихідний потік

### Опис

```methodsynopsis
public SplFileObject::fpassthru(): int
```

Читає дані з файлу з поточної позиції до кінця файлу та поміщає їх у буфер вихідного потоку.

Якщо ви вже записали якісь дані у файл і вам необхідно повернутися на початкову позицію, файловий покажчик можна скинути методом [SplFileObject::rewind()](splfileobject.rewind.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість символів, прочитаних із дескриптора `handle` та переданих на висновок.

### Приклади

**Приклад #1 Приклад використання** SplFileObject::fpassthru()\*\*\*\*

```php
<?php

// Открыть файл в режиме чтения двоичных данных
$file = new SplFileObject("./img/ok.png", "rb");

// Отправить правильные заголовки
header("Content-Type: image/png");
header("Content-Length: " . $file->getSize());

// Вывести изображение и завершить работу скрипта
$file->fpassthru();
exit;

?>
```

### Дивіться також

-   [fpassthru()](function.fpassthru.md) \- Виводить всі дані з файлового покажчика, що залишилися.
