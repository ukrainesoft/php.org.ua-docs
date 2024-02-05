---
navigation:
  - function.pcntl-rfork.md: « pcntl\_rfork
  - function.pcntl-signal-dispatch.md: pcntl\_signal\_dispatch »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_setpriority
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_setpriority

(PHP 5, PHP 7, PHP 8)

pcntl\_setpriority — Змінити пріоритет процесу

### Опис

```methodsynopsis
pcntl_setpriority(int $priority, ?int $process_id = null, int $mode = PRIO_PROCESS): bool
```

**pcntl\_setpriority()** ставить пріоритет процесу, вказаному в аргументі `process_id`

### Список параметрів

`priority`

Как правило приоритет`priority` - це значення в інтервалі від `-20`до`20`Приоритет по умолчанию равен , при тому що нижче числове значення означає вищий пріоритет процесу. Оскільки рівні пріоритету процесів відрізняються в різних типах операційних систем та версіях їх ядер, будь ласка, ознайомтеся з вашим системним посібником getpriority(2) для отримання детальної інформації про специфіку роботи функції у вашій системі.

`process_id`

Якщо не вказано, буде використано ідентифікатор поточного процесу.

`mode`

Може набувати значення однієї з констант **`PRIO_PGRP`** **`PRIO_USER`** **`PRIO_PROCESS`** **`PRIO_DARWIN_BG`** або **`PRIO_DARWIN_THREAD`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `process_id` тепер допускає значення null. |

### Дивіться також

-   [pcntl\_getpriority()](function.pcntl-getpriority.md) \- Отримати значення пріоритету процесу
-   **pcntl\_setpriority()**
