---
navigation:
  - function.shmop-size.html: « shmopsize
  - class.shmop.md: Shmop »
  - index.md: PHP Manual
  - ref.shmop.md: 'Пам''ять, що розділяється (shared)'
title: shmopwrite
---
# shmopwrite

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

shmopwrite — Запис даних у пам'ять, що розділяється.

### Опис

```methodsynopsis
shmop_write(Shmop $shmop, string $data, int $offset): int
```

**shmopwrite()** записує рядкові дані в ділянку пам'яті, що розділяється.

### Список параметрів

`shmop`

Ресурс блоку пам'яті, що повертається функцією [shmopopen()](function.shmop-open.md)

`data`

Рядкові дані для розміщення в пам'яті

`offset`

Визначає, де місця пам'яті слід розпочати запис даних.

### Значення, що повертаються

Розмір записаних даних, переданих через параметр `data`

### список змін

| Версия | Описание |
| --- | --- |
|  | До PHP 8.0.0 у разі виникнення помилки поверталося **`false`** |
|  | Параметр `shmop` чекає на екземпляр [Shmop](class.shmop.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Запис даних у ділянку пам'яті, що розділяється**

```php
<?php
$shm_bytes_written = shmop_write($shm_id, $my_string, 0);
?>
```

У цьому прикладі в пам'ять міститься вміст рядкової змінної `$my_string`, після чого змінна `$shm_bytes_written` міститиме розмір фактично записаних даних.

### Дивіться також

-   [shmopread()](function.shmop-read.md) - Читання даних з ділянки пам'яті, що розділяється
