Обробка

-   [« Threaded::chunk](threaded.chunk.html)
    
-   [Threaded::extend »](threaded.extend.html)
    
-   [PHP Manual](index.html)
    
-   [Threaded](class.threaded.html)
    
-   Обробка
    

# Threaded::count

(PECL pthreads >= 2.0.0)

Threaded::count — Обробка

### Опис

```methodsynopsis
public Threaded::count(): int
```

Повертає кількість властивостей цього об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Підрахунок властивостей об'єкта**

```php
<?php
$safe = new Threaded();

while (count($safe) < 10) {
    $safe[] = count($safe);
}

var_dump(count($safe));
?>
```

Результат виконання цього прикладу:

```
int(10)
```