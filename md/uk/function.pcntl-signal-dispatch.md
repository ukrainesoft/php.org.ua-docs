Викликає обробники для сигналів, що очікують.

-   [« pcntl\_setpriority](function.pcntl-setpriority.html)
    
-   [pcntl\_signal\_get\_handler »](function.pcntl-signal-get-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Викликає обробники для сигналів, що очікують.
    

# pcntlsignaldispatch

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsignaldispatch — Викликає обробники для сигналів очікування

### Опис

```methodsynopsis
pcntl_signal_dispatch(): bool
```

Функція **pcntlsignaldispatch()** викликає обробники сигналів, встановлені функцією [pcntl\_signal()](function.pcntl-signal.html), для кожного сигналу, що очікує.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **pcntlsignaldispatch()****

```php
<?php
echo "Установка обработчика сигнала SIGHUP...\n";
pcntl_signal(SIGHUP,  function($signo) {
     echo "Вызван обработчик сигнала SIGHUP\n";
});

echo "Посылаем сигнал SIGHUP самому себе...\n";
posix_kill(posix_getpid(), SIGHUP);

echo "Отравка всех сигналов...\n";
pcntl_signal_dispatch();

echo "Завершено.\n";

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

-   [pcntl\_signal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntl\_sigprocmask()](function.pcntl-sigprocmask.html) - Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.html) - Очікування сигналів
-   [pcntl\_sigtimedwait()](function.pcntl-sigtimedwait.html) - Очікує сигнали протягом заданого часу