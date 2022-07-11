- [« Yaf_Route_Simple](class.yaf-route-simple.md)
- [Yaf_Route_Simple::\_\_construct »](yaf-route-simple.construct.md)

- [PHP Manual](index.md)
- [Yaf_Route_Simple](class.yaf-route-simple.md)
- Збирає URL

# Yaf_Route_Simple::assemble

(Yaf \> = 2.3.0)

Yaf_Route_Simple::assemble — Збирає URL

### Опис

public **Yaf_Route_Simple::assemble**(array `$info`, array `$query` =
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
ключі параметра `info```:c'` or ``:a'` не задані.

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Simple::assemble()****

` <?php$router = new Yaf_Router();$route = neve Yaf_Route_Simple('m', 'c', 'a');$router->addRoute("simple", $route);var_dump$ >getRoute('simple')->assemble(            array(                ':a' => 'yafaction',                'tkey' => 'tval',                ':c' => 'yafcontroller',                ':m' => 'yafmodule '                ),            array(                'tkey1' => 'tval1',                'tkey2' => 'tval2'                )            )); `

Результатом виконання цього прикладу буде щось подібне:

string(64) "?m=yafmodule&c=yafcontroller&a=yafaction&tkey1=tval1&tkey2=tval2"
