Отримати поточний рядок файлу

-   [« SplFileObject::construct](splfileobject.construct.html)
    
-   [SplFileObject::eof »](splfileobject.eof.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримати поточний рядок файлу
    

# SplFileObject::current

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::current — Отримати поточний рядок файлу

### Опис

```methodsynopsis
public SplFileObject::current(): string|array|false
```

Витягує поточний рядок файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Витягує поточний рядок файлу. Якщо встановлено прапор \*\*`SplFileObject::READ_CSV`\*\*Цей метод буде розбирати рядок, як дані CSV, і поверне масив. Якщо кінець файлу досягнуто, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **SplFileObject::current()****

```php
<?php
$file = new SplFileObject(__FILE__);
foreach ($file as $k => $line) {
   echo ($file->key() + 1) . ': ' . $file->current();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1: <?php
2: $file = new SplFileObject(__FILE__);
3: foreach ($file as $line) {
4:     echo ($file->key() + 1) . ': ' . $file->current();
5: }
6: ?>
```

### Дивіться також

-   [SplFileObject::key()](splfileobject.key.html) - Отримати номер рядка
-   [SplFileObject::seek()](splfileobject.seek.html) - Переклад файлового покажчика на заданий рядок
-   [SplFileObject::next()](splfileobject.next.html) - Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.html) - Перемотування файлового покажчика на початок файлу
-   [SplFileObject::valid()](splfileobject.valid.html) - Перевіряє, чи кінець файлу (EOF) досягнуто.