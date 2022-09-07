---
navigation:
  - function.gc-enable.md: « gcenable
  - function.gc-mem-caches.md: гкmemcaches »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: гкenabled
---
# гкenabled

(PHP 5> = 5.3.0, PHP 7, PHP 8)

гкenabled — Повертає поточний стан збирача циклічних посилань

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

**Приклад #1 Приклад використання **гкenabled()****

```php
<?php
if(gc_enabled()) gc_collect_cycles();
?>
```

### Дивіться також

-   [Сборка мусора](features.gc.md)
