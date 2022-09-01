---
navigation:
  - function.realpath-cache-get.html: « realpathcacheget
  - function.realpath.html: realpath »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: realpathcachesize
---
# realpathcachesize

(PHP 5> = 5.3.2, PHP 7, PHP 8)

realpathcachesize — Отримує розмір кеша realpath

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

**Приклад #1 Приклад використання **realpathcachesize()****

```php
<?php
var_dump(realpath_cache_size());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(412)
```

### Дивіться також

-   [realpathcacheget()](function.realpath-cache-get.md) - Отримує записи з кеша realpath
-   Конфігураційна опція [realpathcachesize](ini.core.html#ini.realpath-cache-size)
