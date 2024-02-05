---
navigation:
  - function.sodium-crypto-generichash-keygen.md: « sodium\_crypto\_generichash\_keygen
  - function.sodium-crypto-generichash.md: sodium\_crypto\_generichash »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_generichash\_update
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_generichash\_update

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_generichash\_update — Додати повідомлення до хешу

### Опис

```methodsynopsis
sodium_crypto_generichash_update(string &$state, string $message): true
```

Додає повідомлення до внутрішнього хеш-стану.

### Список параметрів

`state`

Возвращаемое значение[sodium\_crypto\_generichash\_init()](function.sodium-crypto-generichash-init.md)

`message`

Дані для додавання до стану хешування.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_generichash\_update()\*\*\*\*

```php
<?php
$messages = [random_bytes(32), random_bytes(32), random_bytes(16)];
$state = sodium_crypto_generichash_init();
foreach ($messages as $message) {
    sodium_crypto_generichash_update($state, $message);
}
$final = sodium_crypto_generichash_final($state);
var_dump(sodium_bin2hex($final));

$allAtOnce = sodium_crypto_generichash(implode('', $messages));
var_dump(sodium_bin2hex($allAtOnce));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(64) "e16e28bbbbcc39d9f5b1cbc33c41f1d217808640103e57a41f24870f79831e04"
string(64) "e16e28bbbbcc39d9f5b1cbc33c41f1d217808640103e57a41f24870f79831e04"
```
