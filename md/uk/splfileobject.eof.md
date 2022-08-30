Перевіряє, чи кінець файлу досягнуто.

-   [« SplFileObject::current](splfileobject.current.html)
    
-   [SplFileObject::fflush »](splfileobject.fflush.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Перевіряє, чи кінець файлу досягнуто.
    

# SplFileObject::eof

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::eof — Перевіряє, чи кінець файлу досягнуто.

### Опис

```methodsynopsis
public SplFileObject::eof(): bool
```

Визначає, чи було досягнуто кінця файлу

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо кінець файлу було досягнуто; **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::eof()****

```php
<?php
$file = new SplFileObject("fruits.txt");
while ( ! $file->eof()) {
    echo $file->fgets();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple
banana
cherry
date
elderberry
```

### Дивіться також

-   [SplFileObject::valid()](splfileobject.valid.html) - Перевіряє, чи кінець файлу (EOF) досягнуто.
-   [feof()](function.feof.html) - Перевіряє, чи кінець файлу досягнуто