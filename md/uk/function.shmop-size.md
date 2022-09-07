---
navigation:
  - function.shmop-read.md: « shmopread
  - function.shmop-write.md: shmopwrite »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmopsize
---
# shmopsize

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

shmopsize — Повертає розмір блоку в пам'яті, що розділяється.

### Опис

```methodsynopsis
shmop_size(Shmop $shmop): int
```

**shmopsize()** використовується для отримання розміру блоку пам'яті, що розділяється в байтах.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmopopen()](function.shmop-open.md)

### Значення, що повертаються

Результатом є ціле число, що відображає кількість байт, зарезервованих в пам'яті для конкретного блоку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Отримання розміру блоку пам'яті, що розділяється**

```php
<?php
$shm_size = shmop_size($shm_id);
?>
```

У наведеному прикладі показано отримання розміру блоку з ідентифікатором `$shm_id` та його збереження в `$shm_size`
