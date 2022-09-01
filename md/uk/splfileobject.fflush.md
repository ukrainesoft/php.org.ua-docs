---
navigation:
  - splfileobject.eof.html: '« SplFileObject::eof'
  - splfileobject.fgetc.html: 'SplFileObject::fgetc »'
  - index.html: PHP Manual
  - class.splfileobject.html: SplFileObject
title: 'SplFileObject::fflush'
---
# SplFileObject::fflush

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fflush — Скидає буфер виводу у файл

### Опис

```methodsynopsis
public SplFileObject::fflush(): bool
```

Примусове записування всіх буферизованих даних у файл.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fflush()****

```php
<?php
$file = new SplFileObject('misc.txt', 'r+');
$file->rewind();
$file->fwrite("Foo");
$file->fflush();
$file->ftruncate($file->ftell());
?>
```

### Дивіться також

-   [SplFileObject::fwrite()](splfileobject.fwrite.html) - Запис у файл
