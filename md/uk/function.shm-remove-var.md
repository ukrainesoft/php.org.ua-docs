---
navigation:
  - function.shm-put-var.md: « shm\_put\_var
  - function.shm-remove.md: shm\_remove »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_remove\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_remove\_var

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_remove\_var — Видалення змінної з пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_remove_var(SysvSharedMemory $shm, int $key): bool
```

Видаляє змінну із заданим ключем `key` та звільняє зайняту пам'ять.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_remove()](function.shm-remove.md) \- Видаляє пам'ять, що розділяється, з систем Unix
