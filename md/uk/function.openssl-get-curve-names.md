---
navigation:
  - function.openssl-get-cipher-methods.md: « openssl\_get\_cipher\_methods
  - function.openssl-get-md-methods.md: openssl\_get\_md\_methods »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_get\_curve\_names
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_get\_curve\_names

(PHP 7 >= 7.1.0, PHP 8)

openssl\_get\_curve\_names — список доступних імен кривих для ECC

### Опис

```methodsynopsis
openssl_get_curve_names(): array|false
```

Повертає список доступних кривих імен для використання в еліптичній криптографії (ECC) для операцій з відкритим/закритим ключем. Дві найбільш стандартизовані/підтримувані криві: *prime256v1*(NIST P-256) и*secp384r1*(NIST P-384).

**Наближені еквівалентності розмірів ключів AES, RSA, DSA та ECC**

| AES размер симметричного ключа (Биты) | Размер ключа RSA и DSA (Биты) | Размер ключа ECC (Биты) |
| --- | --- | --- |
| 80 | 1024 | 160 |
| 112 | 2048 | 224 |
| 128 | 3072 | 256 |
| 192 | 7680 | 384 |
| 256 | 15360 | 512 |

[» NIST рекомендує використовувати криві ECC як мінімум у 256 біт](http://dx.doi.org/10.6028/NIST.SP.800-57pt1r4)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив з доступними іменами кривих або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** openssl\_get\_curve\_names()\*\*\*\*

```php
<?php
$curve_names = openssl_get_curve_names();
print_r($curve_names);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => secp112r1
    [1] => secp112r2
    [2] => secp128r1
    [3] => secp128r2
    [4] => secp160k1
    [5] => secp160r1
    [6] => secp160r2
    [7] => secp192k1
    [8] => secp224k1
    [9] => secp224r1
    [10] => secp256k1
    [11] => secp384r1
    [12] => secp521r1
    [13] => prime192v1
    [14] => prime192v2
    [15] => prime192v3
    [16] => prime239v1
    [17] => prime239v2
    [18] => prime239v3
    [19] => prime256v1
    [20] => sect113r1
    [21] => sect113r2
    [22] => sect131r1
    [23] => sect131r2
    [24] => sect163k1
    [25] => sect163r1
    [26] => sect163r2
    [27] => sect193r1
    [28] => sect193r2
    [29] => sect233k1
    [30] => sect233r1
    [31] => sect239k1
    [32] => sect283k1
    [33] => sect283r1
    [34] => sect409k1
    [35] => sect409r1
    [36] => sect571k1
    [37] => sect571r1
    [38] => c2pnb163v1
    [39] => c2pnb163v2
    [40] => c2pnb163v3
    [41] => c2pnb176v1
    [42] => c2tnb191v1
    [43] => c2tnb191v2
    [44] => c2tnb191v3
    [45] => c2pnb208w1
    [46] => c2tnb239v1
    [47] => c2tnb239v2
    [48] => c2tnb239v3
    [49] => c2pnb272w1
    [50] => c2pnb304w1
    [51] => c2tnb359v1
    [52] => c2pnb368w1
    [53] => c2tnb431r1
    [54] => wap-wsg-idm-ecid-wtls1
    [55] => wap-wsg-idm-ecid-wtls3
    [56] => wap-wsg-idm-ecid-wtls4
    [57] => wap-wsg-idm-ecid-wtls5
    [58] => wap-wsg-idm-ecid-wtls6
    [59] => wap-wsg-idm-ecid-wtls7
    [60] => wap-wsg-idm-ecid-wtls8
    [61] => wap-wsg-idm-ecid-wtls9
    [62] => wap-wsg-idm-ecid-wtls10
    [63] => wap-wsg-idm-ecid-wtls11
    [64] => wap-wsg-idm-ecid-wtls12
    [65] => Oakley-EC2N-3
    [66] => Oakley-EC2N-4
    [67] => brainpoolP160r1
    [68] => brainpoolP160t1
    [69] => brainpoolP192r1
    [70] => brainpoolP192t1
    [71] => brainpoolP224r1
    [72] => brainpoolP224t1
    [73] => brainpoolP256r1
    [74] => brainpoolP256t1
    [75] => brainpoolP320r1
    [76] => brainpoolP320t1
    [77] => brainpoolP384r1
    [78] => brainpoolP384t1
    [79] => brainpoolP512r1
    [80] => brainpoolP512t1
)
```
