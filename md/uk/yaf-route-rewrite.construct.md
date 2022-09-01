---
navigation:
  - yaf-route-rewrite.assemble.html: '« YafRouteRewrite::assemble'
  - yaf-route-rewrite.route.html: 'YafRouteRewrite::route »'
  - index.md: PHP Manual
  - class.yaf-route-rewrite.html: YafRouteRewrite
title: 'YafRouteRewrite::construct'
---
# YafRouteRewrite::construct

(Yaf >=1.0.0)

YafRouteRewrite::construct - Конструктор класу YafRouteRewrite

### Опис

public **YafRouteRewrite::construct**(string `$match`, array `$route`, array `$verify`

### Список параметрів

`match`

Шаблон, який буде використовуватися для порівняння запиту URI, якщо він не збігається, [YafRouteRewrite](class.yaf-route-rewrite.html) поверне **`false`**

Ви можете використовувати: стиль імені для іменування збігаються сегментів і використовувати для відповідності іншим сегментам URL.

`route`

Коли шаблон збігу відповідає запиту uri, [YafRouteRewrite](class.yaf-route-rewrite.html) використовуватиме це, щоб вирішити, який модуль/контролер/дія є пунктом призначення.

Будь-який модуль/контролер/дія в цьому масиві не є обов'язковою, якщо ви не призначите конкретне значення, вона буде перенаправлена ​​на значення за промовчанням.

`verify`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafRouteRewrite()****

```php
<?php
   /**
    * Добавить маршрут перезаписи в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_rewrite(
           "/product/:name/:id/*", //запрос на совпадение с ведущим "/product"
           array(
               'controller' => "product",  //маршрут к контроллеру product,
           ),
        )
    );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* для http://yourdomain.com/product/foo/22/foo/bar
 * результатом маршрута будут следующие значения:
 */
array(
  "controller" => "product",
  "module"     => "index", //(по умолчанию)
  "action"     => "index", //(по умолчанию)
)

/**
 * и параметры запроса:
 */
array(
  "name" => "foo",
  "id"   => 22,
  "foo"  => bar
)
```

**Приклад #2 Приклад використання **YafRouteRewrite()****

```php
<?php
   /**
    * Добавьте маршрут перезаписи в стек маршрутов Yaf_Router, вызвав addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "rewrite",        //маршрут Yaf_Route_Rewrite
           "match" => "/user-list/:id", //совпадение только по /user/list/?/
           "route" => array(
               'controller' => "user",  //маршрут к контроллеру user,
               'action'     => "list",  //маршрут к действию list
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* для http://yourdomain.com/user-list/22
 * результатом маршрута будут следующие значения:
 */
array(
  "controller" => "user",
  "action"     => "list",
  "module"     => "index", //(по умолчанию)
)

/**
 * и параметры запроса:
 */
array(
  "id"   => 22,
)
```

**Приклад #3 Приклад використання **YafRouteRewrite(as of 2.3.0)()****

```php
<?php
   /**
    * Добавить переписать маршрут использовать результат поиска как имя м/к/д
    */
    $config = array(
        "name" => array(
           "type"  => "rewrite",
           "match" => "/user-list/:a/:id", //совпадение только по /user-list/*
           "route" => array(
               'controller' => "user",   //маршрут к контроллеру user,
               'action'     => ":a",     //маршрут к действию :a
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* для http://yourdomain.com/user-list/list/22
 * результатом маршрута будут следующие значения:
 */
array(
  "controller" => "user",
  "action"     => "list",
  "module"     => "index", //(по умолчанию)
)

/**
 * и параметры запроса:
 */
array(
  "id"   => 22,
)
```

### Дивіться також

-   [YafRouter::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора
-   [YafRouter::addConfig()](yaf-router.addconfig.html) - Додає налаштовані маршрути до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.html)
-   [YafRouteSupervar](class.yaf-route-supervar.html)
-   [YafRouteSimple](class.yaf-route-simple.html)
-   [YafRouteRegex](class.yaf-route-regex.html)
-   [YafRouteMap](class.yaf-route-map.html)
