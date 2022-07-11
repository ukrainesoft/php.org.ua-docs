- [« Yaf_Route_Supervar](class.yaf-route-supervar.md)
- [Yaf_Route_Supervar::\_\_construct »](yaf-route-supervar.construct.md)

- [PHP Manual](index.md)
- [Yaf_Route_Supervar](class.yaf-route-supervar.md)
- Збирає URL

# Yaf_Route_Supervar::assemble

(Yaf \> = 2.3.0)

Yaf_Route_Supervar::assemble — Збирає URL

### Опис

public **Yaf_Route_Supervar::assemble**(array `$info`, array `$query` =
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

**Приклад #1 Приклад використання **Yaf_Route_Supervar::assemble()****

` <?php$router== new Yaf_Router();$route = new Yaf_Route_Supervar('r');$router->addRoute("supervar", $route);var_dump($router->getRoute(' >assemble(        array(              ':a' => 'yafaction',              'tkey' => 'tval',              ':c' => 'yafcontroller',              ':m' => 'yafmodule'        ),        array(              'tkey1' => 'tval1',              'tkey2' => 'tval2'        )));try {var_dump($router->getRoute('supervar')->assemble(        array(              ':a' => 'yafaction',              'tkey ' => 'tval',              ':m' => 'yafmodule'        ),        array(              'tkey1' => 'tval1',              'tkey2' => 'tval2',              1 => array(),        )));} catch (Exception $e) {    var_dump($e->getMessage());} `

Результатом виконання цього прикладу буде щось подібне:

string(%d) "?r=/yafmodule/yafcontroller/yafaction&tkey1=tval1&tkey2=tval2"
string(%d) "Ви потребуєте відповідь на контролері ':c'"
