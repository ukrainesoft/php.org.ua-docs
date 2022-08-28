Попросити libevent не використати певний метод події

-   [« EventConfig](class.eventconfig.html)
    
-   [EventConfig::\_\_construct »](eventconfig.construct.html)
    
-   [PHP Manual](index.html)
    
-   [EventConfig](class.eventconfig.html)
    
-   Попросити libevent не використати певний метод події
    

# EventConfig::avoidMethod

(PECL event >= 1.2.6-beta)

EventConfig::avoidMethod — Попросити libevent не використовувати певний метод події

### Опис

```methodsynopsis
public
   EventConfig::avoidMethod(
    string
     $method
   ): bool
```

Попросити libevent не використовувати певний метод події (бекенд). Дивіться [» Создание базы события](http://www.wangafu.net/~nickm/libevent-book/Ref2_eventbase.html#_creating_an_event_base)

### Список параметрів

`method`

Метод бекенда, який потрібно ігнорувати. Дивіться [константы EventConfig](class.eventconfig.html#eventconfig.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **Приклад використання EventConfig::avoidMethod()****

```php
<?php
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "Метод 'select' будет игнорироваться\n";
}
?>
```

### Дивіться також

-   [EventBase::\_\_construct()](eventbase.construct.html) - Конструктор об'єкту EventBase