---
navigation:
  - function.yaml-emit-file.md: « yaml\_emit\_file
  - function.yaml-parse-file.md: yaml\_parse\_file »
  - index.md: PHP Manual
  - ref.yaml.md: Функції Yaml
title: yaml\_emit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaml\_emit

(PECL yaml >= 0.5.0)

yaml\_emit — Повертає YAML-подання значення

### Опис

```methodsynopsis
yaml_emit(    mixed $data,    int $encoding = YAML_ANY_ENCODING,    int $linebreak = YAML_ANY_BREAK,    array $callbacks = null): string
```

Повертає YAML-подання переданих у параметрі `data` даних.

### Список параметрів

`data`

Дані `data` для кодування. Параметр може бути будь-якого типу, крім ресурсу (resource).

`encoding`

Вихідне кодування вибирається з **`YAML_ANY_ENCODING`** **`YAML_UTF8_ENCODING`** **`YAML_UTF16LE_ENCODING`** **`YAML_UTF16BE_ENCODING`**

`linebreak`

Символ перекладу рядка у виводі **`YAML_ANY_BREAK`** **`YAML_CR_BREAK`** **`YAML_LN_BREAK`** **`YAML_CRLN_BREAK`**

`callbacks`

Обробники контенту для створення вузлів YAML. Асоціативний масив (array), де як ключі використовуються імена класів, а як значення callback-функції ([callable](language.types.callable.md)), які створюватимуть вузли для цих класів. Більше подробиць можна дізнатись у розділі про [публікуючі callback-функції](yaml.callbacks.emit.md)

### Значення, що повертаються

Повертає YAML-закодований рядок (string) у разі успішного виконання.

### список змін

| Версия | Опис |
| --- | --- |
| PECL yaml 1.1.0 | Добавлен параметр`callbacks` |

### Приклади

**Приклад #1 Приклад використання** yaml\_emit()\*\*\*\*

```php
<?php
$addr = array(
    "given" => "Chris",
    "family"=> "Dumars",
    "address"=> array(
        "lines"=> "458 Walkman Dr.
        Suite #292",
        "city"=> "Royal Oak",
        "state"=> "MI",
        "postal"=> 48046,
      ),
  );
$invoice = array (
    "invoice"=> 34843,
    "date"=> 980208000,
    "bill-to"=> $addr,
    "ship-to"=> $addr,
    "product"=> array(
        array(
            "sku"=> "BL394D",
            "quantity"=> 4,
            "description"=> "Basketball",
            "price"=> 450,
          ),
        array(
            "sku"=> "BL4438H",
            "quantity"=> 1,
            "description"=> "Super Hoop",
            "price"=> 2392,
          ),
      ),
    "tax"=> 251.42,
    "total"=> 4443.52,
    "comments"=> "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.",
  );
var_dump(yaml_emit($invoice));
?>
```

Висновок наведеного прикладу буде схожим на:

```
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
```

### Дивіться також

-   [yaml\_emit\_file()](function.yaml-emit-file.md) \- Відправляє YAML-подання значення файлу
-   [yaml\_parse()](function.yaml-parse.md) \- Розбирає потік YAML
