---
navigation:
  - eventbase.free.md: '« EventBase::free'
  - eventbase.getmethod.md: 'EventBase::getMethod »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::getFeatures'
---
# EventBase::getFeatures

(PECL event >= 1.2.6-beta)

EventBase::getFeatures — Повертає бітову маску підтримуваних функцій

### Опис

```methodsynopsis
public
   EventBase::getFeatures(): int
```

Повертає бітову маску підтримуваних функцій

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітову маску функцій, що підтримуються. Дивіться константи [EventConfig::FEATURE](class.eventconfig.md#eventconfig.constants)

### Приклади

**Приклад #1 Приклад використання **EventBase::getFeatures()****

```php
<?php
// Avoiding "select" method
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}

$base = new EventBase($cfg);

echo "Характеристики:\n";
$features = $base->getFeatures();
($features & EventConfig::FEATURE_ET) and print("ET - edge-triggered IO\n");
($features & EventConfig::FEATURE_O1) and print("O1 - O(1) operation for adding/deletting events\n");
($features & EventConfig::FEATURE_FDS) and print("FDS - arbitrary file descriptor types, and not just sockets\n");
?>
```

### Дивіться також

-   [EventBase::getMethod()](eventbase.getmethod.md) - Повертає використовуваний метод події
-   [EventConfig](class.eventconfig.md)
