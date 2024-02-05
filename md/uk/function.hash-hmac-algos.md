---
navigation:
  - function.hash-hkdf.md: « hash\_hkdf
  - function.hash-hmac-file.md: hash\_hmac\_file »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_hmac\_algos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_hmac\_algos

(PHP 7 >= 7.2.0, PHP 8)

hash\_hmac\_algos — Повертає список зареєстрованих алгоритмів хешування, які застосовуються для hash\_hmac

### Опис

```methodsynopsis
hash_hmac_algos(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив зі списком підтримуваних функцією [hash\_hmac()](function.hash-hmac.md)алгоритмов хеширования.

### Приклади

**Пример #1 Пример использования**hash\_hmac\_algos()\*\*\*\*

```php
<?php
print_r(hash_hmac_algos());
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => md2
    [1] => md4
    [2] => md5
    [3] => sha1
    [4] => sha224
    [5] => sha256
    [6] => sha384
    [7] => sha512/224
    [8] => sha512/256
    [9] => sha512
    [10] => sha3-224
    [11] => sha3-256
    [12] => sha3-384
    [13] => sha3-512
    [14] => ripemd128
    [15] => ripemd160
    [16] => ripemd256
    [17] => ripemd320
    [18] => whirlpool
    [19] => tiger128,3
    [20] => tiger160,3
    [21] => tiger192,3
    [22] => tiger128,4
    [23] => tiger160,4
    [24] => tiger192,4
    [25] => snefru
    [26] => snefru256
    [27] => gost
    [28] => gost-crypto
    [29] => haval128,3
    [30] => haval160,3
    [31] => haval192,3
    [32] => haval224,3
    [33] => haval256,3
    [34] => haval128,4
    [35] => haval160,4
    [36] => haval192,4
    [37] => haval224,4
    [38] => haval256,4
    [39] => haval128,5
    [40] => haval160,5
    [41] => haval192,5
    [42] => haval224,5
    [43] => haval256,5
)
```

### Примітки

> **Зауваження** :
> 
> До PHP 7.2.0 єдиним варіантом отримати список підтримуваних алгоритмів було викликати функцію [hash\_algos()](function.hash-algos.md), яка також повертала алгоритми, що не підтримуються [hash\_hmac()](function.hash-hmac.md)

### Дивіться також

-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [hash\_algos()](function.hash-algos.md) \- Повертає список зареєстрованих алгоритмів хешування
