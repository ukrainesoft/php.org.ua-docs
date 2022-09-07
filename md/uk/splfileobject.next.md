---
navigation:
  - splfileobject.key.md: '« SplFileObject::key'
  - splfileobject.rewind.md: 'SplFileObject::rewind »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::next'
---
# SplFileObject::next

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::next — Читати наступний рядок

### Опис

```methodsynopsis
public SplFileObject::next(): void
```

Перехід до наступного рядка у файлі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::next()****

```php
<?php
// Читаем файл построчно
$file = new SplFileObject("misc.txt");
while (!$file->eof()) {
    echo $file->current();
    $file->next();
}
?>
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.md) - Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.md) - Отримати номер рядка
-   [SplFileObject::seek()](splfileobject.seek.md) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::rewind()](splfileobject.rewind.md) - Перемотування файлового покажчика на початок файлу
-   [SplFileObject::valid()](splfileobject.valid.md) - Перевіряє, чи кінець файлу (EOF) досягнуто.
