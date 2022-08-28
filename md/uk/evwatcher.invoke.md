Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій

-   [« EvWatcher::getLoop](evwatcher.getloop.html)
    
-   [EvWatcher::keepalive »](evwatcher.keepalive.html)
    
-   [PHP Manual](index.html)
    
-   [EvWatcher](class.evwatcher.html)
    
-   Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій
    

# EvWatcher::invoke

(PECL ev >= 0.2.0)

EvWatcher::invoke — Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій

### Опис

```methodsynopsis
public
   EvWatcher::invoke(
    int
     $revents
   ): void
```

Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій.

### Список параметрів

`revents`

Бітова маска спостерігача [принятых событий](class.ev.html#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.