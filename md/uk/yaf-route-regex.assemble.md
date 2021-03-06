- [« Yaf_Route_Regex](class.yaf-route-regex.md)
- [Yaf_Route_Regex::\_\_construct »](yaf-route-regex.construct.md)

- [PHP Manual](index.md)
- [Yaf_Route_Regex](class.yaf-route-regex.md)
- Сформувати URL-адресу

# Yaf_Route_Regex::assemble

(Yaf \> = 2.3.0)

Yaf_Route_Regex::assemble — Сформувати URL-адресу

### Опис

public **Yaf_Route_Regex::assemble**(array `$info`, array `$query` = ?):
?string

Сформувати URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string) у разі успішного виконання або **`null`**
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Regex::assemble()****

` <?php$router = new Yaf_Router();$route  = new Yaf_Route_Regex(            "#^/product/([^/]+)/([^/])+#",            array(                'controller' => " product",  //маршрут на контроллер product,                ),            array(),            array(),            '/:m/:c/:a'        );$router->addRoute("regex", $route);var_dump($ router->getRoute('regex')->assemble(            array(                ':m' => 'module',                ':c' => 'controller',                ':a' => 'action'                ),            array(                'tkey1 ' => 'tval1',                'tkey2' =>                'tval2'                )            )        ); `

Результатом виконання цього прикладу буде щось подібне:

string(49) "/module/controller/action?tkey1=tval1&tkey2=tval2"
