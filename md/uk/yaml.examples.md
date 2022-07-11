- [«Зумовлені константи](yaml.constants.md)
- [Callback-функції »](yaml.callbacks.md)

- [PHP Manual](index.md)
- [Yaml](book.yaml.md)
- Приклади

# Приклади

**Приклад #1 Приклад роботи з Yaml**

` <?php$addr = array(    "given" => "Chris",    "family"=> "Dumars",    "address"=> array(        "lines"=> "458 Walkman Dr.        Suite #292",        " city"=> "Royal Oak",        "state"=> "MI",        "postal"=> 48046,      ),  );$invoice = array (    "invoice"=> 34843,    "date"=> "2001-01 -23",    "bill-to"=> $addr,    "ship-to"=> $addr,    "product"=> array(        array(            "sku"=> "BL394D",            "quantity"=> 4,            " description"=> "Basketball",            "price"=> 450,          ),        array(            "sku"=> "BL4438H",            "quantity"=> 1,            "description"=> "Super Hoop",            "price"=> 2392,          ),      ),    "tax"=> 251.42,    "total"=> 4443.52,    "comments"=> "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.",    );// создание YAML- подання замовлення$yaml = yaml_emit($invoice);var_dump($yaml);// перетворення YAML назад в PHP-змінну$parsed = yaml_parse($yaml);// перевірка на ори а і результату конвертації в YAML і обратноvar_dump($parsed == $invoice);?> `

Результатом виконання цього прикладу буде щось подібне:

string(631) "---
invoice: 34843
date: "2001-01-23"
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
bool(true)
