Вимикає всі воркери

-   [« Pool::resize](pool.resize.html)
    
-   [Pool::submit »](pool.submit.html)
    
-   [PHP Manual](index.html)
    
-   [Pool](class.pool.html)
    
-   Вимикає всі воркери
    

# Pool::shutdown

(PECL pthreads >= 2.0.0)

Pool::shutdown - Вимикає всі воркери

### Опис

```methodsynopsis
public Pool::shutdown(): void
```

Вимикає всіх воркерів у пулі. Буде заблоковано доти, доки всі надіслані завдання не будуть виконані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Вимкнення пулу**

```php
<?php
class Task extends Threaded
{
    public function run()
    {
        usleep(500000);
    }
}

$pool = new Pool(4);

for ($i = 0; $i < 10; ++$i) {
    $pool->submit(new Task());
}

$pool->shutdown(); // пока все отправленные задачи не завершат выполнение
```