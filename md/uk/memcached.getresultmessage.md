Повертає повідомлення, що описує результат виконання останньої операції

-   [« Memcached::getResultCode](memcached.getresultcode.html)
    
-   [Memcached::getServerByKey »](memcached.getserverbykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Повертає повідомлення, що описує результат виконання останньої операції
    

# Memcached::getResultMessage

(PECL memcached >= 1.0.0)

Memcached::getResultMessage — Повертає повідомлення, що описує результат виконання останньої операції

### Опис

```methodsynopsis
public Memcached::getResultMessage(): string
```

**Memcached::getResultMessage()** повертає рядок, що описує результуючий код виконання останнього методу Memcached.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повідомлення, що описує результат виконання останньої операції Memcached.

### Приклади

**Приклад #1 Приклад використання **Memcached::getResultMessage()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->add('foo', 'bar'); // первое добавление успешно выполнится
$m->add('foo', 'bar');
echo $m->getResultMessage(),"\n";
?>
```

Результат виконання цього прикладу:

```
NOT STORED
```