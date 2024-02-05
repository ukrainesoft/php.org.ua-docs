---
navigation:
  - function.gc-enable.md: « gc\_enable
  - function.gc-mem-caches.md: gc\_mem\_caches »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: gc\_enabled
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gc\_enabled

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gc\_enabled — Повертає поточний стан збирача циклічних посилань

### Опис

```methodsynopsis
gc_enabled(): bool
```

Повертає поточний стан збирача циклічних посилань.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо збирач сміття включений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** gc\_enabled()\*\*\*\*

```php
<?php
if(gc_enabled()) gc_collect_cycles();
?>
```

### Дивіться також

-   [Складання сміття](features.gc.md)
