---
navigation:
  - pharfileinfo.destruct.md: '« PharFileInfo::destruct'
  - pharfileinfo.getcompressedsize.md: 'PharFileInfo::getCompressedSize »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::getCRC32'
---
# PharFileInfo::getCRC32

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getCRC32 — Отримати контрольну суму CRC32

### Опис

```methodsynopsis
public PharFileInfo::getCRC32(): int
```

Повертає контрольну суму [crc32()](function.crc32.md) для файлу у Phar-архіві.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Контрольна сума [crc32()](function.crc32.md) для файлу у Phar-архіві.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо не вдалося верифікувати контрольну суму CRC32. Цього практично неможливо досягти при звичайній роботі, оскільки контрольна сума перевіряється під час читання та запису файлу.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::getCRC32()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    echo $file->getCRC32();
} catch (Exception $e) {
    echo 'Операции записи на my.phar завершились ошибкой: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
3633523372
```
