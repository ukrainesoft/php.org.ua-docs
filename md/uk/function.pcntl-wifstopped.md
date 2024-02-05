---
navigation:
  - function.pcntl-wifsignaled.md: « pcntl\_wifsignaled
  - function.pcntl-wstopsig.md: pcntl\_wstopsig »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_wifstopped
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_wifstopped

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

pcntl\_wifstopped — Перевірити, чи зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wifstopped(int $status): bool
```

Перевіряє, чи зупинено дочірній процес, що викликало повернення; це можливо лише якщо функція [pcntl\_waitpid()](function.pcntl-waitpid.md) викликалася з опцією `WUNTRACED`

### Список параметрів

`status`

Параметр`status` — це параметр статусу, який передається для успішного виклику функції [pcntl\_waitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо дочірній процес викликав повернення зараз зупинено. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntl\_waitpid()](function.pcntl-waitpid.md) \- Очікує чи повертає статус породженого дочірнього процесу
