---
navigation:
  - function.pcntl-wexitstatus.md: « pcntl\_wexitstatus
  - function.pcntl-wifsignaled.md: pcntl\_wifsignaled »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wifexited
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wifexited

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wifexited — Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Опис

```methodsynopsis
pcntl_wifexited(int $status): bool
```

Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо код завершення дочірнього процесу відповідає нормальному завершенню. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wexitstatus()](function.pcntl-wexitstatus.md) \- Отримати код повернення завершеного дочірнього процесу
