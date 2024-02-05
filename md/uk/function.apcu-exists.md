---
navigation:
  - function.apcu-entry.md: « apcu\_entry
  - function.apcu-fetch.md: apcu\_fetch »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_exists

(PECL apcu >= 4.0.0)

apcu\_exists — Перевіряє, чи є записи

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

**Пример #1 Пример использования**apcu\_exists()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

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

-   [apcu\_cache\_info()](function.apcu-cache-info.md) \- Витягує закешовану інформацію зі сховища APCu
-   [apcu\_fetch()](function.apcu-fetch.md) \- Витягує з кеша збережену змінну
