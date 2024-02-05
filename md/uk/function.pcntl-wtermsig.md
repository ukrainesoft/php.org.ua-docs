---
navigation:
  - function.pcntl-wstopsig.md: « pcntl\_wstopsig
  - book.posix.md: POSIX »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wtermsig
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wtermsig

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wtermsig — Отримати сигнал, через який було примусово завершено дочірній процес

### Опис

```methodsynopsis
pcntl_wtermsig(int $status): int|false
```

Повертає номер сигналу, через який примусово завершили дочірній процес. Має сенс тільки якщо [pcntl\_wifsignaled()](function.pcntl-wifsignaled.md) повернула **`true`**

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_signal()](function.pcntl-signal.md) \- Встановлення оброблювача сигналу
-   [pcntl\_wifsignaled()](function.pcntl-wifsignaled.md) \- Перевірити, чи код завершення процесу завершення по сигналу
