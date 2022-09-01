---
navigation:
  - function.pcntl-wexitstatus.html: pcntlwexitstatus
  - function.pcntl-wifsignaled.html: pcntlwifsignaled »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwifexited
---
# pcntlwifexited

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwifexited — Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Опис

```methodsynopsis
pcntl_wifexited(int $status): bool
```

Перевіряє, чи код завершення процесу відповідає нормальному завершенню.

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо код завершення дочірнього процесу відповідає нормальному завершенню. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwexitstatus()](function.pcntl-wexitstatus.md) - Отримати код повернення завершеного дочірнього процесу
