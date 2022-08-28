Перевіряє, чи був цикл обробки подій завершено

-   [« EventBase::gotExit](eventbase.gotexit.html)
    
-   [EventBase::loop »](eventbase.loop.html)
    
-   [PHP Manual](index.html)
    
-   [EventBase](class.eventbase.html)
    
-   Перевіряє, чи був цикл обробки подій завершено
    

# EventBase::gotStop

(PECL event >= 1.2.6-beta)

EventBase::gotStop — Перевіряє, чи завершився цикл обробки подій.

### Опис

```methodsynopsis
public
   EventBase::gotStop(): bool
```

Перевіряє, чи був цикл обробки подій завершено за допомогою [EventBase::stop()](eventbase.stop.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цикл обробки подій було завершено за допомогою [EventBase::stop()](eventbase.stop.html) . В іншому випадку - **`false`**

### Дивіться також

-   [EventBase::exit()](eventbase.exit.html) - Припиняє відправлення подій
-   [EventBase::stop()](eventbase.stop.html) - Повідомляє eventbase припинити відправку подій
-   [EventBase::gotExit()](eventbase.gotexit.html) - Перевіряє, чи був цикл обробки подій завершений