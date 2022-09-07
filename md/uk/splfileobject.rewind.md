---
navigation:
  - splfileobject.next.md: '« SplFileObject::next'
  - splfileobject.seek.md: 'SplFileObject::seek »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::rewind'
---
# SplFileObject::rewind

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::rewind — Перемотування файлового покажчика на початок файлу

### Опис

```methodsynopsis
public SplFileObject::rewind(): void
```

Перемотує файловий покажчик на початок файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо покажчик не можна перемотати, буде викинуто виняток [RuntimeException](class.runtimeexception.md)

### Приклади

**Приклад #1 Приклад використання **SplFileObject::rewind()****

```php
<?php
$file = new SplFileObject("misc.txt");

// Проход по всему файлу
foreach ($file as $line) { }

// Перемотка на первую строку
$file->rewind();

// Вывод первой строки
echo $file->current();
?>
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.md) - Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.md) - Отримати номер рядка
-   [SplFileObject::seek()](splfileobject.seek.md) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::next()](splfileobject.next.md) - Читати наступний рядок
-   [SplFileObject::valid()](splfileobject.valid.md) - Перевіряє, чи кінець файлу (EOF) досягнуто.
