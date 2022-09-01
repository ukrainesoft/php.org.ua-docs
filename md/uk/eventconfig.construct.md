---
navigation:
  - eventconfig.avoidmethod.md: '« EventConfig::avoidMethod'
  - eventconfig.requirefeatures.md: 'EventConfig::requireFeatures »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::construct'
---
# EventConfig::construct

(PECL event >= 1.2.6-beta)

EventConfig::construct — Створити об'єкт EventConfig

### Опис

```methodsynopsis
public
   EventConfig::__construct()
```

Створює об'єкт EventConfig, який можна передати до конструктора [EventBase::construct()](eventbase.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventConfig](class.eventconfig.md)

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

-   [EventBase::construct()](eventbase.construct.md) - Конструктор об'єкту EventBase
