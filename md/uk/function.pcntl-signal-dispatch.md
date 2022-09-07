---
navigation:
  - function.pcntl-setpriority.md: pcntlsetpriority
  - function.pcntl-signal-get-handler.md: pcntlsignalgethandler »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlsignaldispatch
---
# pcntlsignaldispatch

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsignaldispatch — Викликає обробники для сигналів очікування

### Опис

```methodsynopsis
pcntl_signal_dispatch(): bool
```

Функція **pcntlsignaldispatch()** викликає обробники сигналів, встановлені функцією [pcntlsignal()](function.pcntl-signal.md), для кожного сигналу, що очікує.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **pcntlsignaldispatch()****

```php
<?php
echo "Установка обработчика сигнала SIGHUP...\n";
pcntl_signal(SIGHUP,  function($signo) {
     echo "Вызван обработчик сигнала SIGHUP\n";
});

echo "Посылаем сигнал SIGHUP самому себе...\n";
posix_kill(posix_getpid(), SIGHUP);

echo "Отравка всех сигналов...\n";
pcntl_signal_dispatch();

echo "Завершено.\n";

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Установка обработчика сигнала SIGHUP...
Посылаем сигнал SIGHUP самому себе...
Отравка всех сигналов...
Вызван обработчик сигнала SIGHUP
Завершено.
```

### Дивіться також

-   [pcntlsignal()](function.pcntl-signal.md) - Встановлення оброблювача сигналу
-   [pcntlsigprocmask()](function.pcntl-sigprocmask.md) - Задає та витягує список сигналів, що блокуються.
-   [pcntlsigwaitinfo()](function.pcntl-sigwaitinfo.md) - Очікування сигналів
-   [pcntlsigtimedwait()](function.pcntl-sigtimedwait.md) - Очікує сигнали протягом заданого часу
