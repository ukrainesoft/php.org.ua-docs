---
navigation:
  - function.sem-remove.md: « sem\_remove
  - function.shm-detach.md: shm\_detach »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_attach
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_attach

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_attach — Створює або відкриває сегмент пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_attach(int $key, ?int $size = null, int $permissions = 0666): SysvSharedMemory|false
```

**shm\_attach()** повертає ідентифікатор, який можна використовувати для доступу до пам'яті System V, що розділяється, по заданому ключу `key`. Перший виклик створює сегмент розміром `size` та опціональними бітами прав доступу `permissions`

Наступний виклик **shm\_attach()** з тим же ключем `key` поверне інший екземпляр [SysvSharedMemory](class.sysvsharedmemory.md), але вони обидва будуть вказувати на один і той же сегмент пам'яті, що розділяється. Параметри `size`и`permissions` будуть проігноровані.

### Список параметрів

`key`

Числовий ідентифікатор сегмента пам'яті

`size`

Розмір пам'яті. Якщо не заданий, то за умовчанням використовуватиметься `sysvshm.init_mem` у php.ini. Якщо не заданий і він, то 10000 байт.

`permissions`

Опціональні біти прав доступу. Типово 0666.

### Значення, що повертаються

Повертає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше повертався ресурс (resource). |
| 8.0.0 | `size` тепер допускає значення null. |

### Дивіться також

-   [shm\_detach()](function.shm-detach.md) \- Вимикається від сегмента пам'яті, що розділяється
-   [ftok()](function.ftok.md) \- Перетворює шлях та ідентифікатор проекту на ключ System V IPC
