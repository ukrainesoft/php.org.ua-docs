---
navigation:
  - function.shmop-open.md: « shmop\_open
  - function.shmop-size.md: shmop\_size »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmop\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shmop\_read

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

shmop\_read — Читання даних з ділянки пам'яті, що розділяється

### Опис

```methodsynopsis
shmop_read(Shmop $shmop, int $offset, int $size): string
```

**shmop\_read()** повертає рядкові дані, що зберігаються в ділянці пам'яті, що розділяється.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmop\_open()](function.shmop-open.md)

`offset`

Усунення, з якого починається читання; повинно бути більше або дорівнює нулю і менше або дорівнює фактичному розміру сегмента пам'яті, що розділяється.

`size`

Кількість байтів для читання; має бути більше або дорівнює нулю, а сума `offset`и`size` повинна бути меншою або дорівнює фактичному розміру сегмента пам'яті, що розділяється . зчитує байти `shmop_size($shmid) - $start`

### Значення, що повертаються

Повертає строкові дані або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо параметр `offset`или`size` знаходяться поза допустимим діапазоном, викидається виняток [ValueError](class.valueerror.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікували ресурс (resource). |
| 8.0.0 | Якщо параметр `offset`или`size` знаходяться поза допустимим діапазоном, викидається виняток [ValueError](class.valueerror.md); раніше видавалася помилка рівня **`E_WARNING`** та функція повертала значення **`false`** |

### Приклади

**Приклад #1 Читання даних з ділянки пам'яті, що розділяється**

```php
<?php
$shm_data = shmop_read($shm_id, 0, 50);
?>
```

У наведеному прикладі виконується читання 50 байт з ділянки пам'яті, що розділяється (ідентифікується по `$shm_id`) та розміщення в `$shm_data`

### Дивіться також

-   [shmop\_write()](function.shmop-write.md) \- Запис даних у пам'ять, що розділяється
