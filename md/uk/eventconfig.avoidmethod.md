---
navigation:
  - class.eventconfig.md: « EventConfig
  - eventconfig.construct.md: 'EventConfig::construct »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::avoidMethod'
---
# EventConfig::avoidMethod

(PECL event >= 1.2.6-beta)

EventConfig::avoidMethod — Попросити libevent не використовувати певний метод події

### Опис

```methodsynopsis
public
   EventConfig::avoidMethod(
    string
     $method
   ): bool
```

Попросити libevent не використовувати певний метод події (бекенд). Дивіться [» Створення бази події](http://www.wangafu.net/~nickm/libevent-book/Ref2_eventbase.md#_creating_an_event_base)

### Список параметрів

`method`

Метод бекенда, який потрібно ігнорувати. Дивіться [константи EventConfig](class.eventconfig.md#eventconfig.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **Приклад використання EventConfig::avoidMethod()****

```php
<?php
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}
?>
```

### Дивіться також

-   [EventBase::construct()](eventbase.construct.md) - Конструктор об'єкту EventBase
