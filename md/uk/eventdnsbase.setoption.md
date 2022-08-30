Встановлює значення параметра конфігурації

-   [« EventDnsBase::parseResolvConf](eventdnsbase.parseresolvconf.md)
    
-   [EventDnsBase::setSearchNdots »](eventdnsbase.setsearchndots.md)
    
-   [PHP Manual](index.md)
    
-   [EventDnsBase](class.eventdnsbase.md)
    
-   Встановлює значення параметра конфігурації
    

# EventDnsBase::setOption

(PECL event >= 1.2.6-beta)

EventDnsBase::setOption — Встановлює параметр конфігурації

### Опис

```methodsynopsis
public
   EventDnsBase::setOption(
    string
     $option
   , 
    string
     $value
   ): bool
```

Встановлює параметр конфігурації.

### Список параметрів

`option`

В даний час доступні такі параметри конфігурації: `"ndots"` `"timeout"` `"max-timeouts"` `"max-inflight"` і `"attempts"`

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.