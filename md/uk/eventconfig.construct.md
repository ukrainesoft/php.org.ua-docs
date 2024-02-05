---
navigation:
  - eventconfig.avoidmethod.md: '« EventConfig::avoidMethod'
  - eventconfig.requirefeatures.md: 'EventConfig::requireFeatures »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventConfig::\_\_construct

(PECL event >= 1.2.6-beta)

EventConfig::\_\_construct — Створити об'єкт EventConfig

### Опис

```methodsynopsis
public
   EventConfig::__construct()
```

Створює об'єкт EventConfig, який можна передати до конструктора [EventBase::\_\_construct()](eventbase.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования метода**EventConfig::\_\_construct()\*\*\*\*

```php
<?php

// Игнорируем метод select
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}

// Создаём event_base, связанный с этим конфигом
$base = new EventBase($cfg);

/* Теперь объект $base настроен на игнорирование метода select (бэкенд) */

?>
```

### Дивіться також

-   [EventBase::\_\_construct()](eventbase.construct.md) \- Конструктор об'єкту EventBase
