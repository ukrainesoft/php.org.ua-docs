---
navigation:
  - function.pcntl-sigprocmask.md: pcntlsigprocmask
  - function.pcntl-sigwaitinfo.md: pcntlsigwaitinfo »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntlsigtimedwait
---
# pcntlsigtimedwait

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsigtimedwait — Очікує сигнали протягом заданого часу

### Опис

```methodsynopsis
pcntl_sigtimedwait(    array $signals,    array &$info = [],    int $seconds = 0,    int $nanoseconds = 0): int|false
```

Функція **pcntlsigtimedwait()** поводиться так само як і функція [pcntlsigwaitinfo()](function.pcntl-sigwaitinfo.md) за винятком того, що приймає два додаткові аргументи, `seconds` і `nanoseconds`, які встановлюють верхню межу часу, що скрипт може простоювати.

### Список параметрів

`signals`

Масив очікуваних сигналів.

`info`

`info` містить інформацію про сигнал. Дивіться функцію [pcntlsigwaitinfo()](function.pcntl-sigwaitinfo.md)

`seconds`

Час очікування за секунди.

`nanoseconds`

Час очікування у наносекундах.

### Значення, що повертаються

У разі успішного виконання **pcntlsigtimedwait()** повертає номер сигналу або **`false`** у разі виникнення помилки.

### Дивіться також

-   [pcntlsigprocmask()](function.pcntl-sigprocmask.md) - Задає та витягує список сигналів, що блокуються.
-   [pcntlsigwaitinfo()](function.pcntl-sigwaitinfo.md) - Очікування сигналів
