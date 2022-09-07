---
navigation:
  - function.shmop-open.md: « shmopopen
  - function.shmop-size.md: shmopsize »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmopread
---
# shmopread

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

shmopread — Читання даних з ділянки пам'яті, що розділяється

### Опис

```methodsynopsis
shmop_read(Shmop $shmop, int $offset, int $size): string
```

**shmopread()** повертає рядкові дані, що зберігаються в ділянці пам'яті, що розділяється.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmopopen()](function.shmop-open.md)

`offset`

Визначає з якої позиції починати читання даних.

`size`

Кількість байт для читання . `0` читає `shmop_size($shmid) - $start` байт.

### Значення, що повертаються

Повертає строкові дані або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Читання даних з ділянки пам'яті, що розділяється**

```php
<?php
$shm_data = shmop_read($shm_id, 0, 50);
?>
```

У наведеному прикладі виконується читання 50 байт з ділянки пам'яті, що розділяється (ідентифікується по `$shm_id`) та розміщення в `$shm_data`

### Дивіться також

-   [shmopwrite()](function.shmop-write.md) - Запис даних у пам'ять, що розділяється
