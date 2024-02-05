---
navigation:
  - evembed.set.md: '« EvEmbed::set'
  - class.evfork.md: EvFork »
  - index.md: PHP Manual
  - class.evembed.md: EvEmbed
title: 'EvEmbed::sweep'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvEmbed::sweep

(PECL ev >= 0.2.0)

EvEmbed::sweep — Робить одиночну, неблокуючу розгортку за вбудованим циклом

### Опис

```methodsynopsis
public
   EvEmbed::sweep(): void
```

Робить одиночну, неблокуючу розгортку за вбудованим циклом. Працює аналогічно наступному коду, але є кращим у разі вбудованих циклів:

```php
<?php
$other->start(Ev::RUN_NOWAIT);
?>
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvWatcher::start()](evwatcher.start.md) \- Запускає спостерігача
