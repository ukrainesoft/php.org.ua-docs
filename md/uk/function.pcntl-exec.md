---
navigation:
  - function.pcntl-errno.md: « pcntl\_errno
  - function.pcntl-fork.md: pcntl\_fork »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_exec

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pcntl\_exec — Запуск цієї програми в області поточного процесу

### Опис

```methodsynopsis
pcntl_exec(string $path, array $args = [], array $env_vars = []): bool
```

Запускає програму із переданими аргументами.

### Список параметрів

`path`

`path` шлях до програми або скрипта з коректною вказівкою шляху до інтерпретатора в першому рядку (наприклад, #!/usr/local/bin/perl). Для отримання додаткової інформації зверніться до системного посібника execve(2).

`args`

`args` масив рядків аргументів переданих програмі

`env_vars`

`env_vars` масив рядків, які передані програмі як змінні оточення. Масив формату name => value, де name – ім'я змінної оточення та value – значення змінної оточення.

### Значення, що повертаються

Повертає **`false`**
