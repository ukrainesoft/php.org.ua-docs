---
navigation:
  - function.pcntl-wifexited.md: « pcntl\_wifexited
  - function.pcntl-wifstopped.md: pcntl\_wifstopped »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wifsignaled
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wifsignaled

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wifsignaled — Перевірити, чи код завершення процесу завершення по сигналу відповідає

### Опис

```methodsynopsis
pcntl_wifsignaled(int $status): bool
```

Перевірити, чи код завершення процесу завершення по сигналу.

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає **`true`**, якщо дочірній процес було завершено через неперехоплений сигнал. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_signal()](function.pcntl-signal.md) \- Встановлення оброблювача сигналу
