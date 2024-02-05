---
navigation:
  - function.sodium-crypto-core-ristretto255-sub.md: « sodium\_crypto\_core\_ristretto255\_sub
  - function.sodium-crypto-generichash-init.md: sodium\_crypto\_generichash\_init »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_generichash\_final
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_generichash\_final

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_generichash\_final - Закінчити хешування

### Опис

```methodsynopsis
sodium_crypto_generichash_final(string &$state, int $length = SODIUM_CRYPTO_GENERICHASH_BYTES): string
```

Метод завершення потокового API-інтерфейсу generichash.

### Список параметрів

`state`

Стан хешу, повернутий [sodium\_crypto\_generichash\_init()](function.sodium-crypto-generichash-init.md)

`length`

Довжина виведення.

### Значення, що повертаються

Криптографічний хеш.

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_generichash\_final()\*\*\*\*

```php
<?php
$messages = [random_bytes(32), random_bytes(32), random_bytes(16)];
$state = sodium_crypto_generichash_init('', 32);
foreach ($messages as $message) {
    sodium_crypto_generichash_update($state, $message);
}

$final = sodium_crypto_generichash_final($state, 32);
var_dump(sodium_bin2hex($final));

$allAtOnce = sodium_crypto_generichash(implode('', $messages));
var_dump(sodium_bin2hex($allAtOnce));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(64) "a2939a9163cb7c796ec28e01028489e72475c136b2697ea59e3e760ab4a8ab20"
string(64) "a2939a9163cb7c796ec28e01028489e72475c136b2697ea59e3e760ab4a8ab20"
```
