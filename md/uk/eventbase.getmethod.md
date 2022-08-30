Повертає використовуваний метод події

-   [« EventBase::getFeatures](eventbase.getfeatures.md)
    
-   [EventBase::getTimeOfDayCached »](eventbase.gettimeofdaycached.md)
    
-   [PHP Manual](index.md)
    
-   [EventBase](class.eventbase.md)
    
-   Повертає використовуваний метод події
    

# EventBase::getMethod

(PECL event >= 1.2.6-beta)

EventBase::getMethod — Повертає метод події, що використовується.

### Опис

```methodsynopsis
public
   EventBase::getMethod(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок, що представляє метод події (backend).

### Приклади

**Приклад #1 Приклад використання **EventBase::getMethod()****

```php
<?php
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}

// Создаём базу событий, с конфигурацией
$base = new EventBase($cfg);
echo "Используемый метод события: ", $base->getMethod(), PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
`select' method avoided
Используемый метод события: epoll
```

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.md) - Повертає бітову маску підтримуваних функцій