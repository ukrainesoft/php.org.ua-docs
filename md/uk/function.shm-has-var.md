---
navigation:
  - function.shm-get-var.md: « shm\_get\_var
  - function.shm-put-var.md: shm\_put\_var »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_has\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_has\_var

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

shm\_has\_var — Перевіряє, чи існує конкретний запис

### Опис

```methodsynopsis
shm_has_var(SysvSharedMemory $shm, int $key): bool
```

Перевіряє, чи існує конкретний ключ у сегменті пам'яті, що розділяється.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає **`true`**, якщо запис існує, інакше повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_get\_var()](function.shm-get-var.md) \- Повертає змінну з пам'яті, що розділяється
-   [shm\_put\_var()](function.shm-put-var.md) \- Вставляє або оновлює змінну в пам'яті, що розділяється.
