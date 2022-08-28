Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase

-   [« EventConfig::requireFeatures](eventconfig.requirefeatures.html)
    
-   [EventConfig::setMaxDispatchInterval »](eventconfig.setmaxdispatchinterval.html)
    
-   [PHP Manual](index.html)
    
-   [EventConfig](class.eventconfig.html)
    
-   Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase
    

# EventConfig::setFlags

(PECL event >= 2.0.2-alpha)

EventConfig::setFlags — Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase

### Опис

```methodsynopsis
public
   EventConfig::setFlags(
    int
     $flags
   ): bool
```

Встановлює один або кілька прапорів для налаштування того, які частини можливої ​​EventBase будуть ініціалізовані та як вони працюватимуть.

### Список параметрів

`flags`

Одна з констант `EventBase::LOOP_*`. Дивіться [константы EventBase](class.eventbase.html#eventbase.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.html) - Повертає бітову маску підтримуваних функцій