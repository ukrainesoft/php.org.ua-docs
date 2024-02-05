---
navigation:
  - function.pcntl-waitpid.md: « pcntl\_waitpid
  - function.pcntl-wifexited.md: pcntl\_wifexited »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wexitstatus
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wexitstatus

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wexitstatus — Отримати код повернення завершеного дочірнього процесу

### Опис

```methodsynopsis
pcntl_wexitstatus(int $status): int|false
```

Повертає код повернення завершеного дочірнього процесу. Функція застосовується лише якщо функція [pcntl\_wifexited()](function.pcntl-wifexited.md) повернула **`true`**

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає код повернення дочірнього процесу. Якщо ця функція не підтримується ОС, повертається **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wifexited()](function.pcntl-wifexited.md) \- Перевіряє, чи код завершення процесу відповідає нормальному завершенню
