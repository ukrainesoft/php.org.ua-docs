Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase

-   [« EventConfig::requireFeatures](eventconfig.requirefeatures.md)
    
-   [EventConfig::setMaxDispatchInterval »](eventconfig.setmaxdispatchinterval.md)
    
-   [PHP Manual](index.md)
    
-   [EventConfig](class.eventconfig.md)
    
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

Одна з констант `EventBase::LOOP_*`. Дивіться [константи EventBase](class.eventbase.html#eventbase.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.md) - Повертає бітову маску підтримуваних функцій