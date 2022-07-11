- [« yaml_emit_file](function.yaml-emit-file.md)
- [yaml_parse_file »](function.yaml-parse-file.md)

- [PHP Manual](index.md)
- [Функції Yaml](ref.yaml.md)
- Повертає YAML-подання значення

# yaml_emit

(PECL yaml \>= 0.5.0)

yaml_emit — Повертає YAML-подання значення

### Опис

**yaml_emit**(
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$data`,
int `$encoding` = YAML_ANY_ENCODING,
int `$linebreak` = YAML_ANY_BREAK,
array `$callbacks` = **`null`**
): string

Повертає YAML-подання переданих у параметрі 'data' даних.

### Список параметрів

`data`
Дані `data` для кодування. Параметр може бути будь-якого типу,
винятком ресурсу (resource).

`encoding`
Вихідне кодування вибирається з **`YAML_ANY_ENCODING`**,
**`YAML_UTF8_ENCODING`**, **`YAML_UTF16LE_ENCODING`**,
**`YAML_UTF16BE_ENCODING`**.

`linebreak`
Символ переведення рядка у виведенні **`YAML_ANY_BREAK`**,
**`YAML_CR_BREAK`**, **`YAML_LN_BREAK`**, **`YAML_CRLN_BREAK`**.

callbacks
Обробники контенту для створення вузлів YAML. Асоціативний масив
(array), де як ключі використовуються імена класів, а як
значень callback-функції ([callable](language.types.callable.md)),
які створюватимуть вузли для цих класів. Більше подробиць можна
дізнатися у розділі про [публікуючі callback-функції](yaml.callbacks.emit.md).

### Значення, що повертаються

Повертає YAML-закодований рядок (string) у разі успішного
виконання.

### Список змін

| Версія          | Опис                        |
|-----------------|-----------------------------|
| PECL yaml 1.1.0 | Доданий параметр callbacks. |

### Приклади

**Приклад #1 Приклад використання **yaml_emit()****

` <?php$addr = array(    "given" => "Chris",    "family"=> "Dumars",    "address"=> array(        "lines"=> "458 Walkman Dr.        Suite #292",        " city"=> "Royal Oak",        "state"=> "MI",        "postal"=> 48046,      ),  );$invoice = array (    "invoice"=> 34843,    "date"=> 980208000,    "bill -to"=> $addr,    "ship-to"=> $addr,    "product"=> array(        array(            "sku"=> "BL394D",            "quantity"=> 4,            "description"=> "Basketball ",            "price"=> 450,          ),        array(            "sku"=> "BL4438H",            "quantity"=> 1,            "description"=> "Super Hoop",            "price"=> 2392,          ),      ), "tax"=> 251.42,    "total"=> 4443.52,   "comments"=> "Late afternoon is best. Backup contact is Nancy Billsmer @ | `

Результатом виконання цього прикладу буде щось подібне:

string(628) "---
invoice: 34843
date: 980208000
bill-to:
given: Chris
family: Dumars
address:
lines: |-
458 Walkman Dr.
Suite #292
city: Royal Oak
state: MI
postal: 48046
ship-to:
given: Chris
family: Dumars
address:
lines: |-
458 Walkman Dr.
Suite #292
city: Royal Oak
state: MI
postal: 48046
product:
- sku: BL394D
quantity: 4
description: Basketball
price: 450
- sku: BL4438H
quantity: 1
description: Super Hoop
price: 2392
tax: 251.420000
total: 4443.520000
comments: Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.
...
"

### Дивіться також

- [yaml_emit_file()](function.yaml-emit-file.md) - Відправляє
YAML-представлення значення у файл
- [yaml_parse()](function.yaml-parse.md) - Розбирає потік YAML
