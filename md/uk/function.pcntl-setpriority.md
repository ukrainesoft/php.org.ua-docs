Змінити пріоритет процесу

-   [pcntlrfork](function.pcntl-rfork.html)
    
-   [pcntlsignaldispatch »](function.pcntl-signal-dispatch.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PCNTL](ref.pcntl.md)
    
-   Змінити пріоритет процесу
    

# pcntlsetpriority

(PHP 5, PHP 7, PHP 8)

pcntlsetpriority — Змінити пріоритет процесу

### Опис

```methodsynopsis
pcntl_setpriority(int $priority, ?int $process_id = null, int $mode = PRIO_PROCESS): bool
```

**pcntlsetpriority()** ставить пріоритет процесу, вказаному в аргументі `process_id`

### Список параметрів

`priority`

Як правило, пріоритет `priority` - це значення в інтервалі від `-20` до `20`. Пріоритет за промовчанням дорівнює `0`при тому, що нижче числове значення означає більш високий пріоритет процесу. Оскільки рівні пріоритету процесів відрізняються в різних типах операційних систем та версіях їх ядер, будь ласка, ознайомтеся з вашим системним посібником getpriority(2) для отримання детальної інформації про специфіку роботи функції у вашій системі.

`process_id`

Якщо не вказано, буде використано ідентифікатор поточного процесу.

`mode`

Може набувати значення однієї з констант **`PRIO_PGRP`** **`PRIO_USER`** **`PRIO_PROCESS`** **`PRIO_DARWIN_BG`** або **`PRIO_DARWIN_THREAD`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `process_id` тепер допускає значення null. |

### Дивіться також

-   [pcntlgetpriority()](function.pcntl-getpriority.html) - Отримати значення пріоритету процесу
-   **pcntlsetpriority()**