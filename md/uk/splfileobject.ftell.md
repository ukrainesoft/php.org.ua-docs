---
navigation:
  - splfileobject.fstat.md: '« SplFileObject::fstat'
  - splfileobject.ftruncate.md: 'SplFileObject::ftruncate »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::ftell'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::ftell

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::ftell — Повернути поточну позицію файлового покажчика

### Опис

```methodsynopsis
public SplFileObject::ftell(): int|false
```

Повертає поточну позицію файлового покажчика, яка представляє поточне усунення у файловому потоці.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає позицію файлового покажчика у вигляді цілого чи числа \*\*`false`\*\*в случае ошибки.

### Приклади

**Пример #1 Пример использования**SplFileObject::ftell()\*\*\*\*

```php
<?php
$file = new SplFileObject("/etc/passwd");

// Читаем первую строку
$data = $file->fgets();

// Определяем, где мы?
echo $file->ftell();
?>
```

### Дивіться також

-   [ftell()](function.ftell.md) \- Повертає поточну позицію покажчика читання/запису файлу
