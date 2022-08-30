Перевіряє, чи кінець файлу (EOF) досягнуто.

-   [« SplFileObject::toString](splfileobject.tostring.md)
    
-   [SplTempFileObject »](class.spltempfileobject.md)
    
-   [PHP Manual](index.md)
    
-   [SplFileObject](class.splfileobject.md)
    
-   Перевіряє, чи кінець файлу (EOF) досягнуто.
    

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
// Цикл по файлу
$file = new SplFileObject("file.txt");
while ($file->valid()) {
    echo $file->fgets();
}
?>
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.md) - Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.md) - Отримати номер рядка
-   [SplFileObject::seek()](splfileobject.seek.md) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::next()](splfileobject.next.md) - Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.md) - Перемотування файлового покажчика на початок файлу