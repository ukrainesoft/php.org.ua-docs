---
navigation:
  - function.mcrypt-get-key-size.md: « mcrypt\_get\_key\_size
  - function.mcrypt-list-modes.md: mcrypt\_list\_modes »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_list\_algorithms
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_list\_algorithms

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_list\_algorithms — Отримати список усіх підтримуваних алгоритмів шифрування

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_list_algorithms(string $lib_dir = ini_get("mcrypt.algorithms_dir")): array
```

Отримати список усіх підтримуваних алгоритмів шифрування в заданій директорії `lib_dir`

### Список параметрів

`lib_dir`

Вказує директорію, де розташовані алгоритми. Якщо не встановлено, то буде використано значення директиви `mcrypt.algorithms_dir`из php.ini.

### Значення, що повертаються

Повертає масив підтримуваних алгоритмів.

### Приклади

**Пример #1 Пример использования**mcrypt\_list\_algorithms()\*\*\*\*

```php
<?php
$algorithms = mcrypt_list_algorithms();
print_r($algorithms);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => cast-128
    [1] => gost
    [2] => rijndael-128
    [3] => twofish
    [4] => arcfour
    [5] => cast-256
    [6] => loki97
    [7] => rijndael-192
    [8] => saferplus
    [9] => wake
    [10] => blowfish-compat
    [11] => des
    [12] => rijndael-256
    [13] => serpent
    [14] => xtea
    [15] => blowfish
    [16] => enigma
    [17] => rc2
    [18] => tripledes
)
```
