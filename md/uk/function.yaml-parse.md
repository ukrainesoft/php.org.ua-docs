---
navigation:
  - function.yaml-parse-url.md: « yaml\_parse\_url
  - book.yaf.md: Yaf »
  - index.md: PHP Manual
  - ref.yaml.md: Функції Yaml
title: yaml\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaml\_parse

(PECL yaml >= 0.4.0)

yaml\_parse — Розбирає потік YAML

### Опис

```methodsynopsis
yaml_parse(    string $input,    int $pos = 0,    int &$ndocs = ?,    array $callbacks = null): mixed
```

Конвертує весь потік YAML або його частину і записує змінну.

### Список параметрів

`input`

Рядок для парсингу як потік YAML.

`pos`

Документ для розбору (`-1` для всіх документів, для первого документа, ...).

`ndocs`

Якщо `ndocs` знайдено, тоді він буде замінений на кількість документів у потоці YAML.

`callbacks`

Обробники вмісту для вузлів YAML. Асоціативний масив (array), ключі якого є тегами YAML, а значення callback-функціями ([callable](language.types.callable.md)), які їх оброблятимуть. Докладніше цей механізм описаний у розділі [callback-функції розбору](yaml.callbacks.parse.md)

### Значення, що повертаються

Повертає значення, закодоване в `input`, у відповідному типі PHP або \*\*`false`\*\*в случае возникновения ошибки. Если параметр`pos`равен`-1`, буде повернено масив, що містить один запис для кожного документа, знайденого в потоці.

### Приклади

**Пример #1 Пример использования**yaml\_parse()\*\*\*\*

```php
<?php
$yaml = <<<EOD
---
invoice: 34843
date: "2001-01-23"
bill-to: &id001
  given: Chris
  family: Dumars
  address:
    lines: |-
      458 Walkman Dr.
              Suite #292
    city: Royal Oak
    state: MI
    postal: 48046
    site: zxibit.esy.es
ship-to: *id001
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
EOD;

$parsed = yaml_parse($yaml);
var_dump($parsed);
?>
```

Висновок наведеного прикладу буде схожим на:

```
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
  string(68) "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338."
}
```

### Примітки

**Увага**

Обробляти неперевірене введення користувача, у разі коли для вузлів YAML, що використовують тег `!php/object`, разрешено использование функции[unserialize()](function.unserialize.md), Вкрай небезпечно. Цю поведінку можна вимкнути за допомогою ini-налаштування `yaml.decode_php`

### Дивіться також

-   [yaml\_parse\_file()](function.yaml-parse-file.md) \- Розбирає YAML-потік із файлу
-   [yaml\_parse\_url()](function.yaml-parse-url.md) \- Розбирає YAML-потік із URL
-   [yaml\_emit()](function.yaml-emit.md) \- Повертає YAML-подання значення
