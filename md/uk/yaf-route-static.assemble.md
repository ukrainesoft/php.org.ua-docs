- [« Yaf_Route_Static](class.yaf-route-static.md)
- [Yaf_Route_Static::match »](yaf-route-static.match.md)

- [PHP Manual](index.md)
- [Yaf_Route_Static](class.yaf-route-static.md)
- Збирає URL

# Yaf_Route_Static::assemble

(Yaf \> = 2.3.0)

Yaf_Route_Static::assemble — Збирає URL

### Опис

public **Yaf_Route_Static::assemble**(array `$info`, array `$query` =
?): string

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string).

### Помилки

Викидає
[Yaf_Exception_TypeError](class.yaf-exception-typeerror.md), якщо
ключі параметра `info```:c'` and ``:a'` не задані.

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Static::assemble()****

` <?php$router== new Yaf_Router();$route = new Yaf_Route_Static();$router->addRoute("static", $route);var_dump($router->getRoute('static')-> array(                ':a' => 'yafaction',                'tkey' => 'tval',                ':c' => 'yafcontroller',                ':m' => 'yafmodule'            ),        ));var_dump($router- >getRoute('static')->assemble(            array(                ':a' => 'yafaction',                'tkey' => 'tval',                ':c' => 'yafcontroller',                ':m' => 'yafmodule '            ),            array(                'tkey1' => 'tval1',                'tkey2' => 'tval2'            )        )); `

Результатом виконання цього прикладу буде щось подібне:

string(%d) "/yafmodule/yafcontroller/yafaction"
string(%d) "/yafmodule/yafcontroller/yafaction?tkey1=tval1&tkey2=tval2"
