Обробник setstate

-   [« DateTime::modify](datetime.modify.html)
    
-   [DateTime::setDate »](datetime.setdate.html)
    
-   [PHP Manual](index.html)
    
-   [DateTime](class.datetime.html)
    
-   Обробник setstate
    

# DateTime::setstate

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::setstate - Оброблювач setstate

### Опис

```methodsynopsis
public static DateTime::__set_state(array $array): DateTime
```

Обробник [setstate()](language.oop5.magic.html#object.set-state)

Подібний до методу [DateTimeImmutable::setstate()](datetimeimmutable.set-state.html), крім роботи з об'єктом [DateTime](class.datetime.html)

### Список параметрів

`array`

Масив для ініціалізації.

### Значення, що повертаються

Повертає новий екземпляр класу DateTime.