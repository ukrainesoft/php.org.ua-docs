---
navigation:
  - ref.hash.md: « Функції Hash
  - function.hash-copy.md: hash\_copy »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_algos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_algos

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_algos — Повертає список зареєстрованих алгоритмів хешування

### Опис

```methodsynopsis
hash_algos(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить список алгоритмів хешування, що підтримуються.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Додано підтримку алгоритмів MurmurHash3 і xxHash. |
| 7.4.0 | Додано підтримку для crc32c. |
| 7.1.0 | Додана підтримка для sha512/224, sha512/256, sha3-224, sha3-256, sha3-384 та sha3-512. |

### Приклади

**Приклад #1 Приклад використання** hash\_algos()\*\*\*\*

Починаючи з PHP 8.1.0, **hash\_algos()** повертає наступний список назв алгоритмів хешування.

```php
<?php
print_r(hash_algos());
?>
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
    [29] => adler32
    [30] => crc32
    [31] => crc32b
    [32] => crc32c
    [33] => fnv132
    [34] => fnv1a32
    [35] => fnv164
    [36] => fnv1a64
    [37] => joaat
    [38] => murmur3a
    [39] => murmur3c
    [40] => murmur3f
    [41] => xxh32
    [42] => xxh64
    [43] => xxh3
    [44] => xxh128
    [45] => haval128,3
    [46] => haval160,3
    [47] => haval192,3
    [48] => haval224,3
    [49] => haval256,3
    [50] => haval128,4
    [51] => haval160,4
    [52] => haval192,4
    [53] => haval224,4
    [54] => haval256,4
    [55] => haval128,5
    [56] => haval160,5
    [57] => haval192,5
    [58] => haval224,5
    [59] => haval256,5
)
```

### Дивіться також

-   [hash\_hmac\_algos()](function.hash-hmac-algos.md) \- Повертає список зареєстрованих алгоритмів хешування, які застосовуються для hash\_hmac
