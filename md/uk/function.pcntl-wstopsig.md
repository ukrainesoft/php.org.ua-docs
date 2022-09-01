---
navigation:
  - function.pcntl-wifstopped.html: pcntlwifstopped
  - function.pcntl-wtermsig.html: pcntlwtermsig »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwstopsig
---
# pcntlwstopsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwstopsig — Отримати сигнал, через який було зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wstopsig(int $status): int|false
```

Повертає сигнал, через який було зупинено дочірній процес. Функція має сенс лише якщо [pcntlwifstopped()](function.pcntl-wifstopped.md) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwifstopped()](function.pcntl-wifstopped.md) - Перевірити, чи зупинено дочірній процес
