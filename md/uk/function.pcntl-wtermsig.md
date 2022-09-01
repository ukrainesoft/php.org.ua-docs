---
navigation:
  - function.pcntl-wstopsig.html: pcntlwstopsig
  - book.posix.md: POSIX »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwtermsig
---
# pcntlwtermsig

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwtermsig — Отримати сигнал, через який було примусово завершено дочірній процес

### Опис

```methodsynopsis
pcntl_wtermsig(int $status): int|false
```

Повертає номер сигналу, через який примусово завершили дочірній процес. Має сенс тільки якщо [pcntlwifsignaled()](function.pcntl-wifsignaled.md) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlsignal()](function.pcntl-signal.md) - Встановлення оброблювача сигналу
-   [pcntlwifsignaled()](function.pcntl-wifsignaled.md) - Перевірити, чи код завершення процесу завершення по сигналу
