Синхронізація

-   [« Thread::isStarted](thread.isstarted.md)
    
-   [Thread::start »](thread.start.md)
    
-   [PHP Manual](index.md)
    
-   [Thread](class.thread.md)
    
-   Синхронізація
    

# Thread::join

(PECL pthreads >= 2.0.0)

Thread::join — Синхронізація

### Опис

```methodsynopsis
public Thread::join(): bool
```

Примушує викликаючий контекст чекати, поки вказаний потік завершить виконання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приєднання до зазначеного процесу**

```php
<?php
class My extends Thread {
    public function run() {
        /* ... */
    }
}
$my = new My();
$my->start();
/* ... */
var_dump($my->join());
/* ... */
?>
```

Результат виконання цього прикладу:

```
bool(true)
```