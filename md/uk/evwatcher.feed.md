Подає зазначені події у цикл подій

-   [« EvWatcher::\_\_construct](evwatcher.construct.html)
    
-   [EvWatcher::getLoop »](evwatcher.getloop.html)
    
-   [PHP Manual](index.html)
    
-   [EvWatcher](class.evwatcher.html)
    
-   Подає зазначені події у цикл подій
    

# EvWatcher::feed

(PECL ev >= 0.2.0)

EvWatcher::feed — Подає зазначені події у цикл подій

### Опис

```methodsynopsis
public
   EvWatcher::feed(
    int
     $revents
   ): void
```

Подає зазначені події у цикл подій, ніби зазначена подія сталася для спостерігача.

### Список параметрів

`revents`

Бітова маска спостерігача [принятых событий](class.ev.html#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.