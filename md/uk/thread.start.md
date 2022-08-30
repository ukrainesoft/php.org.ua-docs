Виконання

-   [« Thread::join](thread.join.md)
    
-   [Worker »](class.worker.md)
    
-   [PHP Manual](index.md)
    
-   [Thread](class.thread.md)
    
-   Виконання
    

# Thread::start

(PECL pthreads >= 2.0.0)

Thread::start - Виконання

### Опис

```methodsynopsis
public Thread::start(int $options = ?): bool
```

Запуск нового потоку для виконання реалізованого методу запуску.

### Список параметрів

`options`

Необов'язкова маска констант успадкування за промовчанням PTHREADSINHERITALL.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Запуск потоку**

```php
<?php
class My extends Thread {
    public function run() {
        /** ... **/
    }
}
$my = new My();
var_dump($my->start());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```