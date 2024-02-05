---
navigation:
  - function.shm-has-var.md: « shm\_has\_var
  - function.shm-remove-var.md: shm\_remove\_var »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_put\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_put\_var

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_put\_var — Вставляє або оновлює змінну в пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_put_var(SysvSharedMemory $shm, int $key, mixed $value): bool
```

**shm\_put\_var()** додає або оновлює `value` із заданим ключем `key`

Буде видана помилка (рівня **`E_WARNING`**), якщо `shm` не є допустимим індексом пам'яті SysV або якщо пам'яті, що розділяється, недостатньо для виконання вашого запиту.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

`key`

Ключ змінної.

`value`

Переменная. Могут использоваться все[типи змінної](language.types.md), які підтримують [serialize()](function.serialize.md): зазвичай це означає всі типи, крім ресурсів та деяких внутрішніх об'єктів, які не можуть бути серіалізовані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_get\_var()](function.shm-get-var.md) \- Повертає змінну з пам'яті, що розділяється
-   [shm\_has\_var()](function.shm-has-var.md) \- Перевіряє, чи існує конкретний запис
