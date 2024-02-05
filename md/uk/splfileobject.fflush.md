---
navigation:
  - splfileobject.eof.md: '« SplFileObject::eof'
  - splfileobject.fgetc.md: 'SplFileObject::fgetc »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fflush'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fflush

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fflush — Скидає буфер виводу у файл

### Опис

```methodsynopsis
public SplFileObject::fflush(): bool
```

Примусове записування всіх буферизованих даних у файл.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SplFileObject::fflush()\*\*\*\*

```php
<?php
$file = new SplFileObject('misc.txt', 'r+');
$file->rewind();
$file->fwrite("Foo");
$file->fflush();
$file->ftruncate($file->ftell());
?>
```

### Дивіться також

-   [SplFileObject::fwrite()](splfileobject.fwrite.md) \- Запис у файл
