Надіслати подію сигналу в цикл за замовчуванням

-   [« Ev::feedSignal](ev.feedsignal.html)
    
-   [Ev::iteration »](ev.iteration.html)
    
-   [PHP Manual](index.html)
    
-   [Єв](class.ev.html)
    
-   Надіслати подію сигналу в цикл за замовчуванням
    

# Ev::feedSignalEvent

(No version information available, might only be in Git)

Ev::feedSignalEvent — Надіслати подію сигналу в цикл за замовчуванням

### Опис

```methodsynopsis
final
   public
   static
   Ev::feedSignalEvent(
    int
     $signum
   ): void
```

Надіслати подію сигналу в цикл за замовчуванням. Ev зреагує також, ніби було отримано зазначений сигнал `signal`

### Список параметрів

`signum`

Номер сигналу. Дивіться сторінку man `signal(7)`. Ви можете використовувати константи, експортовані з модуля `pcntl`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::feedSignal()](ev.feedsignal.html) - Передаємо подію сигналу в Ev