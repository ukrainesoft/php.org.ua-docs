Прибрати завдання зі стеку

-   [« Worker::stack](worker.stack.html)
    
-   [Collectable »](class.collectable.html)
    
-   [PHP Manual](index.html)
    
-   [Worker](class.worker.html)
    
-   Прибрати завдання зі стеку
    

# Worker::unstack

(PECL pthreads >= 2.0.0)

Worker::unstack — Прибрати завдання зі стека

### Опис

```methodsynopsis
public Worker::unstack(): int
```

Прибирає перше завдання (найстарішу) зі стека.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий розмір стека.

### список змін

| Версия | Описание |
| --- | --- |
| вз | Прибрано параметр, у якому вказувалося завдання видалення. Тепер завжди видаляється перше завдання. |

### Приклади

**Приклад #1 Видалення об'єктів зі стека Worker**

```php
<?php
$my = new Worker();
$work = new class extends Threaded {};

var_dump($my->stack($work));
var_dump($my->unstack());
```

Результат виконання цього прикладу:

```
int(1)
int(0)
```