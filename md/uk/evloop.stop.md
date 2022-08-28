Зупиняє цикл подій

-   [« EvLoop::stat](evloop.stat.html)
    
-   [EvLoop::suspend »](evloop.suspend.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Зупиняє цикл подій
    

# EvLoop::stop

(PECL ev >= 0.2.0)

EvLoop::stop — Зупиняє цикл подій

### Опис

```methodsynopsis
public
   EvLoop::stop(
    int
     $how
    = ?): void
```

Зупиняє цикл подій

### Список параметрів

`how`

Одна з *Ev::BREAK* [констант](class.ev.html#ev.constants.break-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::run()](evloop.run.html) - Перевіряє події та викликає callback-функції в циклі
-   [Ev::stop()](ev.stop.html) - Зупинити подієвий цикл за замовчуванням