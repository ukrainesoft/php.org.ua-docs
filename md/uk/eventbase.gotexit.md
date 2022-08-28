Перевіряє, чи був цикл обробки подій завершено

-   [« EventBase::getTimeOfDayCached](eventbase.gettimeofdaycached.html)
    
-   [EventBase::gotStop »](eventbase.gotstop.html)
    
-   [PHP Manual](index.html)
    
-   [EventBase](class.eventbase.html)
    
-   Перевіряє, чи був цикл обробки подій завершено
    

# EventBase::gotExit

(PECL event >= 1.2.6-beta)

EventBase::gotExit — Перевіряє, чи завершився цикл обробки подій.

### Опис

```methodsynopsis
public
   EventBase::gotExit(): bool
```

Перевіряє, чи був цикл обробки подій завершено за допомогою [EventBase::exit()](eventbase.exit.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цикл обробки подій завершено за допомогою [EventBase::exit()](eventbase.exit.html) . В інших випадках – **`false`**

### Дивіться також

-   [EventBase::exit()](eventbase.exit.html) - Припиняє відправлення подій
-   [EventBase::stop()](eventbase.stop.html) - Повідомляє eventbase припинити відправку подій
-   [EventBase::gotStop()](eventbase.gotstop.html) - Перевіряє, чи був цикл обробки подій завершений