- [«shmop_read](function.shmop-read.md)
- [shmop_write »](function.shmop-write.md)

- [PHP Manual](index.md)
- [Поділ, що розділяється (shared) пам'ять](ref.shmop.md)
- Повертає розмір блоку в пам'яті, що розділяється

# shmop_size

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

shmop_size — Повертає розмір блоку в пам'яті, що розділяється.

### Опис

**shmop_size**([Shmop](class.shmop.md) `$shmop`): int

**shmop_size()** використовується для отримання розміру блоку, що розділяється
пам'яті у байтах.

### Список параметрів

`shmop`
Ресурс блоку пам'яті, що повертається функцією
[shmop_open()](function.shmop-open.md)

### Значення, що повертаються

Результатом є ціле число, що відображає кількість байт,
зарезервованих в пам'яті для конкретного блоку.

### Список змін

| Версія | Опис                                                                                           |
|--------|------------------------------------------------------------------------------------------------|
| 8.0.0  | Параметр shmop чекає на екземпляр [Shmop](class.shmop.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Отримання розміру блоку пам'яті, що розділяється**

` <?php$shm_size = shmop_size($shm_id);?> `

У наведеному прикладі показано отримання розміру блоку з ідентифікатором
`$shm_id` та його збереження в `$shm_size`.
