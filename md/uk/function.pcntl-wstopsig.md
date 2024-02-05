---
navigation:
  - function.pcntl-wifstopped.md: « pcntl\_wifstopped
  - function.pcntl-wtermsig.md: pcntl\_wtermsig »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wstopsig
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wstopsig

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wstopsig — Отримати сигнал, через який було зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wstopsig(int $status): int|false
```

Повертає сигнал, через який було зупинено дочірній процес. Функція має сенс лише якщо [pcntl\_wifstopped()](function.pcntl-wifstopped.md) повернула **`true`**

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає номер сигналу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wifstopped()](function.pcntl-wifstopped.md) \- Перевірити, чи зупинено дочірній процес
