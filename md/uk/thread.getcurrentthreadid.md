Ідентифікація

-   [« Thread::getCurrentThread](thread.getcurrentthread.md)
    
-   [Thread::getThreadId »](thread.getthreadid.md)
    
-   [PHP Manual](index.md)
    
-   [Thread](class.thread.md)
    
-   Ідентифікація
    

# Thread::getCurrentThreadId

(PECL pthreads >= 2.0.0)

Thread::getCurrentThreadId — Ідентифікація

### Опис

```methodsynopsis
public static Thread::getCurrentThreadId(): int
```

Повертає ідентифікатор поточного потоку, що виконується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий ідентифікатор.

### Приклади

**Приклад #1 Повертає ідентифікатор потоку, що виконується.**

```php
<?php
class My extends Thread {
    public function run() {
        printf("%s является потоком #%lu\n", __CLASS__, Thread::getCurrentThreadId());
    }
}
$my = new My();
$my->start();
?>
```

Результат виконання цього прикладу:

```
My является потоком #123456778899
```