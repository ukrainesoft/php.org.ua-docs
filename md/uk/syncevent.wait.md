Очікує запуску/установки події

-   [« SyncEvent::reset](syncevent.reset.html)
    
-   [SyncReaderWriter »](class.syncreaderwriter.html)
    
-   [PHP Manual](index.html)
    
-   [SyncEvent](class.syncevent.html)
    
-   Очікує запуску/установки події
    

# SyncEvent::wait

(PECL sync >= 1.0.0)

SyncEvent::wait — Очікує запуску/установки події

### Опис

```methodsynopsis
public SyncEvent::wait(int $wait = -1): bool
```

Чекає на запуск об'єкта [SyncEvent](class.syncevent.html)

### Список параметрів

`wait`

Кількість мілісекунд очікування запуску події. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncEvent::wait()****

```php
<?php
// В веб-приложении:
$event = new SyncEvent("GetAppReport");
$event->fire();

// В задании cron:
$event = new SyncEvent("GetAppReport");
$event->wait();
?>
```

### Дивіться також

-   [SyncEvent::fire()](syncevent.fire.html) - Запускає/встановлює подію