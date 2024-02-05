---
navigation:
  - function.pcntl-get-last-error.md: « pcntl\_get\_last\_error
  - function.pcntl-rfork.md: pcntl\_rfork »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_getpriority
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_getpriority

(PHP 5, PHP 7, PHP 8)

pcntl\_getpriority — Отримати значення пріоритету процесу

### Опис

```methodsynopsis
pcntl_getpriority(?int $process_id = null, int $mode = PRIO_PROCESS): int|false
```

\*\*pcntl\_getpriority()\*\*получает значение приоритета для процесса, указанного в аргументе`process_id`. Оскільки рівні пріоритету процесів відрізняються в різних типах операційних систем та версіях їх ядер, будь ласка, ознайомтеся з вашим системним посібником getpriority(2) для отримання детальної інформації про специфіку роботи функції у вашій системі.

### Список параметрів

`process_id`

Якщо не вказано, буде використано ідентифікатор поточного процесу.

`mode`

Може набувати значення однієї з констант **`PRIO_PGRP`** **`PRIO_USER`** **`PRIO_PROCESS`** **`PRIO_DARWIN_BG`**или**`PRIO_DARWIN_THREAD`**

### Значення, що повертаються

**pcntl\_getpriority()** повертає пріоритет процесу, або **`false`** у разі виникнення помилки. Нижче числове значення (в т.ч. негативне) означає більший пріоритет.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `process_id` тепер допускає значення null. |

### Дивіться також

-   [pcntl\_setpriority()](function.pcntl-setpriority.md) \- Змінити пріоритет процесу
