---
navigation:
  - function.realpath-cache-get.md: « realpath\_cache\_get
  - function.realpath.md: realpath »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: realpath\_cache\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# realpath\_cache\_size

(PHP 5 >= 5.3.2, PHP 7, PHP 8)

realpath\_cache\_size — Отримує розмір кеша realpath

### Опис

```methodsynopsis
realpath_cache_size(): int
```

Отримує обсяг пам'яті, який використовується кешем realpath.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає скільки використовується кеш-пам'яті realpath.

### Приклади

**Пример #1 Пример использования**realpath\_cache\_size()\*\*\*\*

```php
<?php
var_dump(realpath_cache_size());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(412)
```

### Дивіться також

-   [realpath\_cache\_get()](function.realpath-cache-get.md) \- Отримує записи з кеша realpath
-   Конфігураційна опція [realpath\_cache\_size](ini.core.md#ini.realpath-cache-size)
