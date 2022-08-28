Створити об'єкт EventConfig

-   [« EventConfig::avoidMethod](eventconfig.avoidmethod.html)
    
-   [EventConfig::requireFeatures »](eventconfig.requirefeatures.html)
    
-   [PHP Manual](index.html)
    
-   [EventConfig](class.eventconfig.html)
    
-   Створити об'єкт EventConfig
    

# EventConfig::construct

(PECL event >= 1.2.6-beta)

EventConfig::construct — Створити об'єкт EventConfig

### Опис

```methodsynopsis
public
   EventConfig::__construct()
```

Створює об'єкт EventConfig, який можна передати до конструктора [EventBase::\_\_construct()](eventbase.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventConfig](class.eventconfig.html)

### Приклади

**Приклад #1 Приклад використання **EventConfig::construct()****

```php
<?php
// Игнорируем метод "select"
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}

// Создаём event_base, связанный с этим конфигом
$base = new EventBase($cfg);

/* Теперь $base настроен на игнорирование метода select (бэкенд) */
?>
```

### Дивіться також

-   [EventBase::\_\_construct()](eventbase.construct.html) - Конструктор об'єкту EventBase