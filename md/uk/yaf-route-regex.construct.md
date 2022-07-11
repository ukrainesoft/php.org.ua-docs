- [« Yaf_Route_Regex::assemble](yaf-route-regex.assemble.md)
- [Yaf_Route_Regex::route »](yaf-route-regex.route.md)

- [PHP Manual](index.md)
- [Yaf_Route_Regex](class.yaf-route-regex.md)
- Конструктор класу Yaf_Route_Regex

# Yaf_Route_Regex::\_\_construct

(Yaf \>=1.0.0)

Yaf_Route_Regex::\_\_construct - Конструктор класу Yaf_Route_Regex

### Опис

public **Yaf_Route_Regex::\_\_construct**(
string `$match`,
array `$route`,
array `$map` = ?,
array `$verify` = ?,
string `$reverse` = ?
)

### Список параметрів

`match`
Готовий шаблон регулярного виразу використовуватиметься для перевірки
відповідності URI запиту; якщо не збігається,
[Yaf_Route_Regex](class.yaf-route-regex.md) поверне **`false`**.

`route`
Коли шаблон відповідності відповідає запиту URI,
[Yaf_Route_Regex](class.yaf-route-regex.md) вирішуватиме, до якого
маршруту m/c/a він належить.

Будь-який з m/c/a у цьому масиві - необов'язковий, якщо ви не призначите
будь-яке значення, він перенаправить на маршрут за промовчанням.

`map`
Масив призначення імені збігам (captures).

`verify`

`reverse`
Рядок, що використовується для формування URL, дивіться
[Yaf_Route_Regex::assemble()](yaf-route-regex.assemble.md).

> **Примітка**:
>
> Цей параметр був представлений у версії 2.3.0

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Regex()****

` <?php   /**    * Добавить маршрут регулярного выражения в стек маршрута Yaf_Router Yaf_Router    */    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",        new Yaf_Route_Regex(           "#^/product/([^ /]+)/([^/])+#", // совпадение с URI запроса, начинающегося с "/product"           array(               'controller' => "product",  // маршрут на контроллер product,           ),           array( 1 => "name",   // теперь вы можете вызвать $request->getParam("name")              2 => "id",     // для получения первого совпадения в шаблоне.           )        )    );?> `

**Приклад #2 Приклад використання **Yaf_Route_Regex (з версії
2.3.0)()****

` <?php   /**    * Использовать результат совпадения в качестве имени MVC    */    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",        new Yaf_Route_Regex(           "#^/product/([^/] +)/([^/])+#i", // совпадение с URI запроса, начинающегося с "/product"           array(              'controller' => ":name", // маршрут на :name, которому соответствует $1 в результате совпадения как имя контроллера           ),           array(              1 => "name",   // теперь вы можете вызвать $request->getParam("name")              2 => "id",     // для получения первого совпадения в шаблоне.           )        ) );?> `

**Приклад #3 Приклад використання **Yaf_Route_Regex з іменованими
збігами (з версії 2.3.0)()****

` <?php   /**    * Использовать результат совпадения в качестве имени MVC    */    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",        new Yaf_Route_Regex(           "#^/product/(?<name> [^/]+)/([^/])+#i", //match request uri leading "/product"           array(           'controller' => ":name", // маршрут на :name,                                    // который называется именем группы совпадения 'name' в результате совпадения как имя контроллера           ),           array(              2 => "id",     // для получения первого совпадения в шаблоне.           )        )    );?> `

**Приклад #4 Приклад використання **Yaf_Route_Regex()****

` <?php   /**    * Добавить маршрут регулярного выражения в стек маршрута Yaf_Router, вызвав addconfig    */    $config = array(        "name" => array(           "type"  => "regex",          // маршрут Yaf_Route_Regex           "match" = > "#(.*)#",         // совпадение с произвольным запросом URI           "route" => array(               'controller' => "product",  // маршрут на контроллер product,               'action'     => "dummy",    / / маршрут на действие dummy           ),           "map" => array(              1 => "uri",   // теперь вы можете вызвать $request->getParam("uri")           ),        ),    ); Yaf_Dispatcher::getInstance()->getRouter()->addConfig(         new Yaf_Config_Simple($config));?> `

### Дивіться також

- [Yaf_Router::addRoute()](yaf-router.addroute.md) - Додає новий
маршрут у маршрутизатор
- [Yaf_Router::addConfig()](yaf-router.addconfig.md) - Додає
налаштовані маршрути на маршрутизатор
- [Yaf_Route_Static](class.yaf-route-static.md)
- [Yaf_Route_Supervar](class.yaf-route-supervar.md)
- [Yaf_Route_Simple](class.yaf-route-simple.md)
- [Yaf_Route_Rewrite](class.yaf-route-rewrite.md)
- [Yaf_Route_Map](class.yaf-route-map.md)
