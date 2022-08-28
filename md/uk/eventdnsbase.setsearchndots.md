Встановлює параметр 'ndots' для пошуку

-   [« EventDnsBase::setOption](eventdnsbase.setoption.html)
    
-   [EventHttp »](class.eventhttp.html)
    
-   [PHP Manual](index.html)
    
-   [EventDnsBase](class.eventdnsbase.html)
    
-   Встановлює параметр 'ndots' для пошуку
    

# EventDnsBase::setSearchNdots

(PECL event >= 1.2.6-beta)

EventDnsBase::setSearchNdots — Встановлює параметр 'ndots' для пошуку

### Опис

```methodsynopsis
public
   EventDnsBase::setSearchNdots(
    int
     $ndots
   ): bool
```

Встановлює параметр **`'ndots'`** для пошуку. Встановлює кількість точок, що при знаходженні імені приводить до того, що перший запит не має пошукового домену.

### Список параметрів

`ndots`

Кількість точок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.