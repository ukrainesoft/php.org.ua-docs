Обробка

-   [« Threaded::run](threaded.run.html)
    
-   [Threaded::synchronized »](threaded.synchronized.html)
    
-   [PHP Manual](index.html)
    
-   [Threaded](class.threaded.html)
    
-   Обробка
    

# Threaded::shift

(PECL pthreads >= 2.0.0)

Threaded::shift — Обробка

### Опис

```methodsynopsis
public Threaded::shift(): mixed
```

Переміщує елемент із таблиці властивостей об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент таблиці властивостей об'єкта.

### Приклади

**Приклад #1 Переміщення першого елемента з таблиці властивостей пов'язаного об'єкта**

```php
<?php
$safe = new Threaded();

while (count($safe) < 10)
    $safe[] = count($safe);

var_dump($safe->shift());
?>
```

Результат виконання цього прикладу:

```
int(0)
```