- [« yaml_parse_url](function.yaml-parse-url.md)
- [Yaf »](book.yaf.md)

- [PHP Manual](index.md)
- [Функції Yaml](ref.yaml.md)
- Розбирає потік YAML

# yaml_parse

(PECL yaml \>= 0.4.0)

yaml_parse - Розбирає потік YAML

### Опис

**yaml_parse**(
string `$input`,
int `$pos` = 0,
int `&$ndocs` = ?,
array `$callbacks` = **`null`**
):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Конвертує весь потік YAML або його частину і записує змінну.

### Список параметрів

`input`
Рядок для парсингу як потік YAML.

`pos`
Документ для розбору (`-1` для всіх документів, `0` для першого
документа, ...).

`ndocs`
Якщо `ndocs` знайдений, тоді він буде замінений на кількість документів
потоці YAML.

callbacks
Обробники вмісту для вузлів YAML. Асоціативний масив (array),
ключі якого є тегами YAML, а значення callback-функціями
([callable](language.types.callable.md)), які будуть їх
обробляти. Докладніше цей механізм описаний у розділі
[callback-функції аналізу](yaml.callbacks.parse.md).

### Значення, що повертаються

Повертає значення, закодоване в `input`, у відповідному типі
PHP або **`false`** у разі виникнення помилки. Якщо параметр `pos`
дорівнює `-1`, буде повернутий масив, що містить по одному запису для
кожного документа, знайденого у потоці.

### Приклади

**Приклад #1 Приклад використання **yaml_parse()****

`<?php$yaml = <<<<EOD---invoice: 34843date: "2001-01-23"bill-to: &id001 given: Chris  family: Dumars address:                Suite #292    city: Royal Oak    state: MI    postal: 48046    site: zxibit.esy.esship-to: *id001product:- sku: BL394D  quantity: 4  description: Basketball  price: 450- sku: BL4438H  quantity: 1  description: Super Hoop price: 2392tax: 251.420000total: 4443.520000comments: Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338....EOD;$parsed = yaml_parse($yaml);var_dump($parsed);?> `

Результатом виконання цього прикладу буде щось подібне:

array(8) {
["invoice"]=>
int(34843)
["date"]=>
string(10) "2001-01-23"
["bill-to"]=>
&array(3) {
["given"]=>
string(5) "Chris"
["family"]=>
string(6) "Dumars"
["address"]=>
array(4) {
["lines"]=>
string(34) "458 Walkman Dr.
Suite #292"
["city"]=>
string(9) "Royal Oak"
["state"]=>
string(2) "MI"
["postal"]=>
int(48046)
}
}
["ship-to"]=>
&array(3) {
["given"]=>
string(5) "Chris"
["family"]=>
string(6) "Dumars"
["address"]=>
array(4) {
["lines"]=>
string(34) "458 Walkman Dr.
Suite #292"
["city"]=>
string(9) "Royal Oak"
["state"]=>
string(2) "MI"
["postal"]=>
int(48046)
}
}
["product"]=>
array(2) {
[0]=>
array(4) {
["sku"]=>
string(6) "BL394D"
["quantity"]=>
int(4)
["description"]=>
string(10) "Basketball"
["price"]=>
int(450)
}
[1]=>
array(4) {
["sku"]=>
string(7) "BL4438H"
["quantity"]=>
int(1)
["description"]=>
string(10) "Super Hoop"
["price"]=>
int(2392)
}
}
["tax"]=>
float(251.42)
["total"]=>
float(4443.52)
["comments"]=>
string(68) "Попередній час є великий. Backup contact is Nancy Billsmer @ 338-4338."
}

### Примітки

**Увага**

Обробляти неперевірене введення користувача, якщо для
вузлів YAML, що використовують тег `!php/object`, дозволено використання
функції [unserialize()](function.unserialize.md), дуже небезпечно. Це
поведінку можна відключити за допомогою ini-налаштування `yaml.decode_php`.

### Дивіться також

- [yaml_parse_file()](function.yaml-parse-file.md) - Розбирає
YAML-потік із файлу
- [yaml_parse_url()](function.yaml-parse-url.md) - Розбирає
YAML-потік з URL
- [yaml_emit()](function.yaml-emit.md) - Повертає
YAML-подання значення
