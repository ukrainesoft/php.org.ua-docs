---
navigation:
  - function.pcntl-get-last-error.html: pcntlgetlasterror
  - function.pcntl-rfork.html: pcntlrfork »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlgetpriority
---
# pcntlgetpriority

(PHP 5, PHP 7, PHP 8)

pcntlgetpriority — Отримати значення пріоритету процесу

### Опис

```methodsynopsis
pcntl_getpriority(?int $process_id = null, int $mode = PRIO_PROCESS): int|false
```

**pcntlgetpriority()** отримує значення пріоритету для процесу, зазначеного в аргументі `process_id`. Оскільки рівні пріоритету процесів відрізняються в різних типах операційних систем та версіях їх ядер, будь ласка, ознайомтеся з вашим системним посібником getpriority(2) для отримання детальної інформації про специфіку роботи функції у вашій системі.

### Список параметрів

`process_id`

Якщо не вказано, буде використано ідентифікатор поточного процесу.

`mode`

Може набувати значення однієї з констант **`PRIO_PGRP`** **`PRIO_USER`** **`PRIO_PROCESS`** **`PRIO_DARWIN_BG`** або **`PRIO_DARWIN_THREAD`**

### Значення, що повертаються

**pcntlgetpriority()** повертає пріоритет процесу, або **`false`** у разі виникнення помилки. Нижче числове значення (в т.ч. негативне) означає більший пріоритет.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание |
| --- | --- |
|  | `process_id` тепер допускає значення null. |

### Дивіться також

-   [pcntlsetpriority()](function.pcntl-setpriority.md) - Змінити пріоритет процесу
