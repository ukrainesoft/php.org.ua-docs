---
navigation:
  - function.pcntl-exec.md: pcntlexec
  - function.pcntl-get-last-error.md: pcntlgetlasterror »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlfork
---
# pcntlfork

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlfork — Розгалужити (fork) поточний запущений процес

### Опис

```methodsynopsis
pcntl_fork(): int
```

Функція **pcntlfork()** створює дочірній процес, який відрізняється від батьківського процесу лише його PID та PPID. Будь ласка, зверніться до вашого системного посібника (man) fork(2) для ознайомлення зі специфікою роботи fork на вашій системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання PID дочірнього процесу буде повернуто в батьківському потоці (thread) запуску і 0 буде повернуто в дочірньому потоці запуску. У разі виникнення помилки, до батьківського контексту буде повернено -1, дочірній процес створений не буде і PHP згенерує відповідну помилку.

### Приклади

**Приклад #1 Приклад **pcntlfork()****

```php
<?php

$pid = pcntl_fork();
if ($pid == -1) {
     die('Не удалось породить дочерний процесс');
} else if ($pid) {
     // Код родительского процесса
     pcntl_wait($status); // Защита против дочерних "Зомби"-процессов
} else {
     // Код дочернего процесса
}

?>
```

### Дивіться також

-   [pcntlrfork()](function.pcntl-rfork.md) - взаємодіє з ресурсами процесу
-   [pcntlwaitpid()](function.pcntl-waitpid.md) - Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlsignal()](function.pcntl-signal.md) - Встановлення оброблювача сигналу
-   [clisetprocesstitle()](function.cli-set-process-title.md) - Встановлює заголовок процесу
