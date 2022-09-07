---
navigation:
  - function.shm-has-var.md: « shmhasvar
  - function.shm-remove-var.md: shmremovevar »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shmputvar
---
# shmputvar

(PHP 4, PHP 5, PHP 7, PHP 8)

shmputvar — Вставляє або оновлює змінну в пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_put_var(SysvSharedMemory $shm, int $key, mixed $value): bool
```

**shmputvar()** додає або оновлює `value` із заданим ключем `key`

Буде видана помилка (рівня **`E_WARNING`**), якщо `shm` не є допустимим індексом пам'яті SysV або якщо пам'яті, що розділяється, недостатньо для виконання вашого запиту.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.md)

`key`

Ключ змінної.

`value`

Змінна. Можуть використовуватися всі [типи змінної](language.types.md), які підтримують [serialize()](function.serialize.md): зазвичай це означає всі типи, крім ресурсів та деяких внутрішніх об'єктів, які не можуть бути серіалізовані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shmgetvar()](function.shm-get-var.md) - Повертає змінну з пам'яті, що розділяється
-   [shmhasvar()](function.shm-has-var.md) - Перевіряє, чи існує конкретний запис
