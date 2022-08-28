Очікує сигнали протягом заданого часу

-   [« pcntl\_sigprocmask](function.pcntl-sigprocmask.html)
    
-   [pcntl\_sigwaitinfo »](function.pcntl-sigwaitinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Очікує сигнали протягом заданого часу
    

# pcntlsigtimedwait

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsigtimedwait — Очікує сигнали протягом заданого часу

### Опис

```methodsynopsis
pcntl_sigtimedwait(    array $signals,    array &$info = [],    int $seconds = 0,    int $nanoseconds = 0): int|false
```

Функція **pcntlsigtimedwait()** поводиться так само як і функція [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.html) за винятком того, що приймає два додаткові аргументи, `seconds` і `nanoseconds`, які встановлюють верхню межу часу, що скрипт може простоювати.

### Список параметрів

`signals`

Масив очікуваних сигналів.

`info`

`info` містить інформацію про сигнал. Дивіться функцію [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.html)

`seconds`

Час очікування за секунди.

`nanoseconds`

Час очікування у наносекундах.

### Значення, що повертаються

У разі успішного виконання **pcntlsigtimedwait()** повертає номер сигналу або **`false`** у разі виникнення помилки.

### Дивіться також

-   [pcntl\_sigprocmask()](function.pcntl-sigprocmask.html) - Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigwaitinfo()](function.pcntl-sigwaitinfo.html) - Очікування сигналів