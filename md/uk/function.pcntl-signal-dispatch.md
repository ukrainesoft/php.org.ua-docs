---
navigation:
  - function.pcntl-setpriority.md: « pcntl\_setpriority
  - function.pcntl-signal-get-handler.md: pcntl\_signal\_get\_handler »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_signal\_dispatch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_signal\_dispatch

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

pcntl\_signal\_dispatch — Викликає обробники для сигналів очікування

### Опис

```methodsynopsis
pcntl_signal_dispatch(): bool
```

Функция**pcntl\_signal\_dispatch()** викликає обробники сигналів, встановлені функцією [pcntl\_signal()](function.pcntl-signal.md), для кожного сигналу, що очікує.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** pcntl\_signal\_dispatch()\*\* :\*\*

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

Висновок наведеного прикладу буде схожим на:

```
Установка обработчика сигнала SIGHUP...
Посылаем сигнал SIGHUP самому себе...
Отравка всех сигналов...
Вызван обработчик сигнала SIGHUP
Завершено.
```

### Дивіться також

-   [pcntl\_signal()](function.pcntl-signal.md) \- Встановлення оброблювача сигналу
-   [pcntl\_sigprocmask()](function.pcntl-sigprocmask.md) \- Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.md) \- Очікування сигналів
-   [pcntl\_sigtimedwait()](function.pcntl-sigtimedwait.md) \- Очікує сигнали протягом заданого часу
