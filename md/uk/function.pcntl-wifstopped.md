---
navigation:
  - function.pcntl-wifsignaled.md: pcntlwifsignaled
  - function.pcntl-wstopsig.md: pcntlwstopsig »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlwifstopped
---
# pcntlwifstopped

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwifstopped — Перевірити, чи зупинено дочірній процес

### Опис

```methodsynopsis
pcntl_wifstopped(int $status): bool
```

Перевіряє, чи зупинено дочірній процес, що викликало повернення; це можливо лише якщо функція [pcntlwaitpid()](function.pcntl-waitpid.md) викликалася з опцією `WUNTRACED`

### Список параметрів

`status`

Параметр `status` - це параметр статусу, який передається для успішного виклику функції [pcntlwaitpid()](function.pcntl-waitpid.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо дочірній процес викликав повернення зараз зупинено. Якщо ні, то повертає **`false`**

### Дивіться також

-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
