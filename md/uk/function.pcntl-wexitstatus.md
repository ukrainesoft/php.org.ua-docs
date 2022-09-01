---
navigation:
  - function.pcntl-waitpid.html: pcntlwaitpid
  - function.pcntl-wifexited.html: pcntlwifexited »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwexitstatus
---
# pcntlwexitstatus

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwexitstatus — Отримати код повернення завершеного дочірнього процесу

### Опис

```methodsynopsis
pcntl_wexitstatus(int $status): int|false
```

Повертає код повернення завершеного дочірнього процесу. Функція застосовується лише якщо функція [pcntlwifexited()](function.pcntl-wifexited.html) повернула **`true`**

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.html)

### Значення, що повертаються

Повертає код повернення дочірнього процесу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.html) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwifexited()](function.pcntl-wifexited.html) - Перевіряє, чи код завершення процесу відповідає нормальному завершенню
