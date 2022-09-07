---
navigation:
  - function.shm-get-var.md: « shmgetvar
  - function.shm-put-var.md: shmputvar »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shmhasvar
---
# shmhasvar

(PHP 5> = 5.3.0, PHP 7, PHP 8)

shmhasvar — Перевіряє, чи існує конкретний запис

### Опис

```methodsynopsis
shm_has_var(SysvSharedMemory $shm, int $key): bool
```

Перевіряє, чи існує конкретний ключ у сегменті пам'яті, що розділяється.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.md)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає **`true`**, якщо запис існує, інакше повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [shmgetvar()](function.shm-get-var.md) - Повертає змінну з пам'яті, що розділяється
-   [shmputvar()](function.shm-put-var.md) - Вставляє або оновлює змінну в пам'яті, що розділяється.
