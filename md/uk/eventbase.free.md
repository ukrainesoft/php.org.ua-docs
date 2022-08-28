Звільняє ресурси, виділені для цієї бази подій

-   [« EventBase::exit](eventbase.exit.html)
    
-   [EventBase::getFeatures »](eventbase.getfeatures.html)
    
-   [PHP Manual](index.html)
    
-   [EventBase](class.eventbase.html)
    
-   Звільняє ресурси, виділені для цієї бази подій
    

# EventBase::free

(PECL event >= 1.10.0)

EventBase::free — Звільняє ресурси, виділені для цієї бази подій

### Опис

```methodsynopsis
public
   EventBase::free(): void
```

Визволяє ресурси, виділені якобов'язок для об'єкта [EventBase](class.eventbase.html)

**Увага**

Метод **EventBase::free()** не руйнує сам об'єкт. Щоб повністю знищити об'єкт, викличте [unset()](function.unset.html) або привласніть **`null`**

Цей метод не звільняє і не від'єднує будь-які події, які на даний момент пов'язані з об'єктом [EventBase](class.eventbase.html), і не закриває їх сокети - будьте обережні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBase::\_\_construct()](eventbase.construct.html) - Конструктор об'єкту EventBase