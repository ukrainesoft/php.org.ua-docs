---
navigation:
  - function.shmop-read.md: « shmop\_read
  - function.shmop-write.md: shmop\_write »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmop\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shmop\_size

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

shmop\_size — Повертає розмір блоку в пам'яті, що розділяється.

### Опис

```methodsynopsis
shmop_size(Shmop $shmop): int
```

**shmop\_size()** використовується для отримання розміру блоку пам'яті, що розділяється в байтах.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmop\_open()](function.shmop-open.md)

### Значення, що повертаються

Результатом є ціле число, що відображає кількість байт, зарезервованих в пам'яті для конкретного блоку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Отримання розміру блоку пам'яті, що розділяється**

```php
<?php
$shm_size = shmop_size($shm_id);
?>
```

У наведеному прикладі показано отримання розміру блоку з ідентифікатором `$shm_id`и его сохранение в`$shm_size`
