Конструктор класу YafRouteRegex

-   [« Yaf\_Route\_Regex::assemble](yaf-route-regex.assemble.html)
    
-   [Yaf\_Route\_Regex::route »](yaf-route-regex.route.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Route\_Regex](class.yaf-route-regex.html)
    
-   Конструктор класу YafRouteRegex
    

# YafRouteRegex::construct

(Yaf >=1.0.0)

YafRouteRegex::construct - Конструктор класу YafRouteRegex

### Опис

public **YafRouteRegex::construct**  
string `$match`  
array `$route`  
array `$map`  
array `$verify`  
string `$reverse`  

### Список параметрів

`match`

Готовий шаблон регулярного виразу використовуватиметься для перевірки відповідності URI запиту; якщо не збігається, [Yaf\_Route\_Regex](class.yaf-route-regex.html) поверне **`false`**

`route`

Коли шаблон відповідності відповідає URI запиту, [Yaf\_Route\_Regex](class.yaf-route-regex.html) буде вирішувати, якого маршруту m/c/a він належить.

Будь-який з m/c/a у цьому масиві - необов'язковий, якщо ви не призначите будь-яке значення, він перенаправить на маршрут за промовчанням.

`map`

Масив призначення імені збігам (captures).

`verify`

`reverse`

Рядок, що використовується для формування URL, дивіться [Yaf\_Route\_Regex::assemble()](yaf-route-regex.assemble.html)

> **Зауваження**
> 
> Цей параметр був представлений у версії 2.3.0

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafRouteRegex()****

```php
<?php
   /**
    * Добавить маршрут регулярного выражения в стек маршрута Yaf_Router Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Regex(
           "#^/product/([^/]+)/([^/])+#", // совпадение с URI запроса, начинающегося с "/product"
           array(
               'controller' => "product",  // маршрут на контроллер product,
           ),
           array(
              1 => "name",   // теперь вы можете вызвать $request->getParam("name")
              2 => "id",     // для получения первого совпадения в шаблоне.
           )
        )
    );
?>
```

**Приклад #2 Приклад використання **YafRouteRegex (з версії 2.3.0)()****

```php
<?php
   /**
    * Использовать результат совпадения в качестве имени MVC
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Regex(
           "#^/product/([^/]+)/([^/])+#i", // совпадение с URI запроса, начинающегося с "/product"
           array(
              'controller' => ":name", // маршрут на :name, которому соответствует $1 в результате совпадения как имя контроллера
           ),
           array(
              1 => "name",   // теперь вы можете вызвать $request->getParam("name")
              2 => "id",     // для получения первого совпадения в шаблоне.
           )
        )
    );
?>
```

**Приклад #3 Приклад використання **YafRouteRegex із іменованими збігами (з версії 2.3.0)()****

```php
<?php
   /**
    * Использовать результат совпадения в качестве имени MVC
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Regex(
           "#^/product/(?<name>[^/]+)/([^/])+#i", //match request uri leading "/product"
           array(
           'controller' => ":name", // маршрут на :name,
                                    // который называется именем группы совпадения 'name' в результате совпадения как имя контроллера
           ),
           array(
              2 => "id",     // для получения первого совпадения в шаблоне.
           )
        )
    );
?>
```

**Приклад #4 Приклад використання **YafRouteRegex()****

```php
<?php
   /**
    * Добавить маршрут регулярного выражения в стек маршрута Yaf_Router, вызвав addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "regex",          // маршрут Yaf_Route_Regex
           "match" => "#(.*)#",         // совпадение с произвольным запросом URI
           "route" => array(
               'controller' => "product",  // маршрут на контроллер product,
               'action'     => "dummy",    // маршрут на действие dummy
           ),
           "map" => array(
              1 => "uri",   // теперь вы можете вызвать $request->getParam("uri")
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

### Дивіться також

-   [Yaf\_Router::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора
-   [Yaf\_Router::addConfig()](yaf-router.addconfig.html) - Додає налаштовані маршрути до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.html)
-   [Yaf\_Route\_Supervar](class.yaf-route-supervar.html)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.html)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.html)
-   [Yaf\_Route\_Map](class.yaf-route-map.html)