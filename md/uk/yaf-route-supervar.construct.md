Призначення construct

-   [« Yaf\_Route\_Supervar::assemble](yaf-route-supervar.assemble.html)
    
-   [Yaf\_Route\_Supervar::route »](yaf-route-supervar.route.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Route\_Supervar](class.yaf-route-supervar.html)
    
-   Призначення construct
    

# YafRouteSupervar::construct

(Yaf >=1.0.0)

YafRouteSupervar::construct - Призначення construct

### Опис

public **YafRouteSupervar::construct**(string `$supervar_name`

[Yaf\_Route\_Supervar](class.yaf-route-supervar.html) схожий на [Yaf\_Route\_Static](class.yaf-route-static.html), Різниця в тому, що [Yaf\_Route\_Supervar](class.yaf-route-supervar.html) шукатиме інформацію про шлях у рядку запиту, а параметр supervarname є ключем.

### Список параметрів

`supervar_name`

Назва ключа.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafRouteSupervar()****

```php
<?php
   /**
    * Добавление маршрута supervar в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute(
        "name",
        new Yaf_Route_Supervar("r")
    );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/** для запроса: http://yourdomain.com/xx/oo/?r=/ctr/act/var/value
  * будет следующий результат:
  */
  array (
    "module"   => index(default),
    "controller" => ctr,
    "action"     => act,
    "params"     => array(
          "var" => value,
     )
  )
```

### Дивіться також

-   [Yaf\_Router::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора
-   [Yaf\_Router::addConfig()](yaf-router.addconfig.html) - Додає налаштовані маршрути до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.html)
-   [Yaf\_Route\_Regex](class.yaf-route-regex.html)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.html)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.html)
-   [Yaf\_Route\_Map](class.yaf-route-map.html)