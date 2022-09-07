---
navigation:
  - function.apcu-entry.md: « apcuentry
  - function.apcu-fetch.md: apcufetch »
  - index.md: PHP Manual
  - ref.apcu.md: Функции APCu
title: apcuexists
---
# apcuexists

(PECL apcu >= 4.0.0)

apcuexists — Перевіряє, чи є записи

### Опис

```methodsynopsis
apcu_exists(mixed $keys): mixed
```

Перевіряє, чи є записи.

### Список параметрів

`keys`

Рядок або масив рядків, що містять ключі для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо ключ існує або **`false`**, якщо ні. Якщо ж було передано масив ключів, то повернеться масив з існуючими ключами, або порожній масив, якщо жодного ключа немає.

### Приклади

**Приклад #1 Приклад використання **apcuexists()****

```php
<?php
$fruit  = 'apple';
$veggie = 'carrot';

apcu_store('foo', $fruit);
apcu_store('bar', $veggie);

if (apcu_exists('foo')) {
    echo "Foo с: ";
    echo apcu_fetch('foo');
} else {
    echo "Foo не существует";
}

echo PHP_EOL;
if (apcu_exists('baz')) {
    echo "Baz не существует.";
} else {
    echo "Baz не существует";
}

echo PHP_EOL;

$ret = apcu_exists(array('foo', 'donotexist', 'bar'));
var_dump($ret);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Foo существует: apple
Baz не существует
array(2) {
  ["foo"]=>
  bool(true)
  ["bar"]=>
  bool(true)
}
```

### Дивіться також

-   [apcucacheinfo()](function.apcu-cache-info.md) - Витягує закешовану інформацію зі сховища APCu
-   [apcufetch()](function.apcu-fetch.md) - Витягує з кеша збережену змінну
