---
navigation:
  - splfileobject.tostring.md: '« SplFileObject::toString'
  - class.spltempfileobject.md: SplTempFileObject »
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::valid'
---
# SplFileObject::valid

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::valid — Перевіряє, чи досягнуто кінець файлу (EOF)

### Опис

```methodsynopsis
public SplFileObject::valid(): bool
```

Перевіряє, чи було досягнуто кінець файлу (EOF).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо EOF не досягнуто, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::valid()****

```php
<?php
// Цикл по файлу
$file = new SplFileObject("file.txt");
while ($file->valid()) {
    echo $file->fgets();
}
?>
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.md) - Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.md) - Отримати номер рядка
-   [SplFileObject::seek()](splfileobject.seek.md) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::next()](splfileobject.next.md) - Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.md) - Перемотування файлового покажчика на початок файлу
