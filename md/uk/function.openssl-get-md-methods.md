---
navigation:
  - function.openssl-get-curve-names.md: « openssl\_get\_curve\_names
  - function.openssl-get-privatekey.md: openssl\_get\_privatekey »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_get\_md\_methods
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_get\_md\_methods

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

openssl\_get\_md\_methods — Отримати список доступних методів хешування

### Опис

```methodsynopsis
openssl_get_md_methods(bool $aliases = false): array
```

Повертає список доступних методів хешування.

### Список параметрів

`aliases`

Якщо хочете, щоб до результуючого масиву були також включені псевдоніми, то встановіть цей параметр у значення **`true`**

### Значення, що повертаються

Масив із доступними методами хешування.

### Приклади

**Приклад #1 Приклад використання** openssl\_get\_md\_methods()\*\*\*\*

Показує, як можуть виглядати доступні методи хешування та їх псевдоніми.

```php
<?php
$digests             = openssl_get_md_methods();
$digests_and_aliases = openssl_get_md_methods(true);
$digest_aliases      = array_diff($digests_and_aliases, $digests);

print_r($digests);

print_r($digest_aliases);

?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => DSA
    [1] => DSA-SHA
    [2] => MD2
    [3] => MD4
    [4] => MD5
    [5] => RIPEMD160
    [6] => SHA
    [7] => SHA1
    [8] => SHA224
    [9] => SHA256
    [10] => SHA384
    [11] => SHA512
    [12] => dsaEncryption
    [13] => dsaWithSHA
    [14] => ecdsa-with-SHA1
    [15] => md2
    [16] => md4
    [17] => md5
    [18] => ripemd160
    [19] => sha
    [20] => sha1
    [21] => sha224
    [22] => sha256
    [23] => sha384
    [24] => sha512
)
Array
(
    [2] => DSA-SHA1
    [3] => DSA-SHA1-old
    [4] => DSS1
    [9] => RSA-MD2
    [10] => RSA-MD4
    [11] => RSA-MD5
    [12] => RSA-RIPEMD160
    [13] => RSA-SHA
    [14] => RSA-SHA1
    [15] => RSA-SHA1-2
    [16] => RSA-SHA224
    [17] => RSA-SHA256
    [18] => RSA-SHA384
    [19] => RSA-SHA512
    [28] => dsaWithSHA1
    [29] => dss1
    [32] => md2WithRSAEncryption
    [34] => md4WithRSAEncryption
    [36] => md5WithRSAEncryption
    [37] => ripemd
    [39] => ripemd160WithRSA
    [40] => rmd160
    [43] => sha1WithRSAEncryption
    [45] => sha224WithRSAEncryption
    [47] => sha256WithRSAEncryption
    [49] => sha384WithRSAEncryption
    [51] => sha512WithRSAEncryption
    [52] => shaWithRSAEncryption
    [53] => ssl2-md5
    [54] => ssl3-md5
    [55] => ssl3-sha1
)
```

### Дивіться також

-   [openssl\_digest()](function.openssl-digest.md) \- Обчислення дайджесту
-   [openssl\_get\_cipher\_methods()](function.openssl-get-cipher-methods.md) \- Отримати список доступних алгоритмів шифрування
