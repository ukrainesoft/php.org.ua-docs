---
navigation:
  - function.shm-detach.md: « shm\_detach
  - function.shm-has-var.md: shm\_has\_var »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_get\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_get\_var

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_get\_var — Повертає змінну з пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_get_var(SysvSharedMemory $shm, int $key): mixed
```

\*\*shm\_get\_var()\*\*возвращает переменную по ключу`key` у зазначеному сегменті пам'яті, що розділяється. Змінна все ще присутня в пам'яті, що розділяється.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає змінну із заданим ключем.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_has\_var()](function.shm-has-var.md) \- Перевіряє, чи існує конкретний запис
-   [shm\_put\_var()](function.shm-put-var.md) \- Вставляє або оновлює змінну в пам'яті, що розділяється.
