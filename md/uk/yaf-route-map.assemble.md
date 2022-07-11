- [« Yaf_Route_Map](class.yaf-route-map.md)
- [Yaf_Route_Map::\_\_construct »](yaf-route-map.construct.md)

- [PHP Manual](index.md)
- [Yaf_Route_Map](class.yaf-route-map.md)
- Збирає URL

# Yaf_Route_Map::assemble

(Yaf \> = 2.3.0)

Yaf_Route_Map::assemble — Збирає URL

### Опис

public **Yaf_Route_Map::assemble**(array `$info`, array `$query` = ?):
string

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string) у разі успішного виконання або **`null`**
у разі виникнення помилки.

### Помилки

Може викинути
[Yaf_Exception_TypeError](class.yaf-exception-typeerror.md).

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Map::assemble()****

` <?php$router== new Yaf_Router();$route = new Yaf_Route_Map();$router->addRoute("map", $route);var_dump($router->getRoute('map')->assemble array(                                ':c' => 'foo_bar'                        ),                        array(                                'tkey1' => 'tval1',                                'tkey2' => 'tval2'                        )                   ));$route = new Yaf_Route_Map(true, '_');$ router->addRoute("map", $route);var_dump($router->getRoute('map')->assemble(                        array(                                ':a' => 'foo_bar'                        ),                        array(                                'tkey1' => ' tval1',                                'tkey2' => 'tval2'                        )                   )); `

Результатом виконання цього прикладу буде щось подібне:

string(%d) "/foo/bar?tkey1=tval1&tkey2=tval2"
string(%d) "/foo/bar/_/tkey1/tval1/tkey2/tval2"
