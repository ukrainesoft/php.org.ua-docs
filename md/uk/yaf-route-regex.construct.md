---
navigation:
  - yaf-route-regex.assemble.md: '« YafRouteRegex::assemble'
  - yaf-route-regex.route.md: 'YafRouteRegex::route »'
  - index.md: PHP Manual
  - class.yaf-route-regex.md: YafRouteRegex
title: 'YafRouteRegex::construct'
---
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

Готовий шаблон регулярного виразу використовуватиметься для перевірки відповідності URI запиту; якщо не збігається, [YafRouteRegex](class.yaf-route-regex.md) поверне **`false`**

`route`

Коли шаблон відповідності відповідає URI запиту, [YafRouteRegex](class.yaf-route-regex.md) буде вирішувати, якого маршруту m/c/a він належить.

Будь-який з m/c/a у цьому масиві - необов'язковий, якщо ви не призначите будь-яке значення, він перенаправить на маршрут за промовчанням.

`map`

Масив призначення імені збігам (captures).

`verify`

`reverse`

Рядок, що використовується для формування URL, дивіться [YafRouteRegex::assemble()](yaf-route-regex.assemble.md)

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

-   [YafRouter::addRoute()](yaf-router.addroute.md) - Додає новий маршрут до маршрутизатора
-   [YafRouter::addConfig()](yaf-router.addconfig.md) - Додає налаштовані маршрути до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.md)
-   [YafRouteSupervar](class.yaf-route-supervar.md)
-   [YafRouteSimple](class.yaf-route-simple.md)
-   [YafRouteRewrite](class.yaf-route-rewrite.md)
-   [YafRouteMap](class.yaf-route-map.md)
