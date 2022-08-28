Скидає ручну подію

-   [« SyncEvent::fire](syncevent.fire.html)
    
-   [SyncEvent::wait »](syncevent.wait.html)
    
-   [PHP Manual](index.html)
    
-   [SyncEvent](class.syncevent.html)
    
-   Скидає ручну подію
    

# SyncEvent::reset

(PECL sync >= 1.0.0)

SyncEvent::reset — Скидає ручну подію

### Опис

```methodsynopsis
public SyncEvent::reset(): bool
```

Скидає об'єкт [SyncEvent](class.syncevent.html), який було запущено/встановлено. Дійсно лише для об'єктів подій зі скиданням вручну.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **SyncEvent::reset()** example**

```php
<?php
// В веб-приложении:
$event = new SyncEvent("DemoApplication", true);
$event->wait();

// В задании cron:
$event = new SyncEvent("DemoApplication", true);
$event->reset();
/* ... Выполнение некоторых задач по обслуживанию ... */
$event->fire();
?>
```

### Дивіться також

-   [SyncEvent::fire()](syncevent.fire.html) - Запускає/встановлює подію
-   **SyncEvent::reset()**
-   [SyncEvent::wait()](syncevent.wait.html) - Очікує запуску/установки події