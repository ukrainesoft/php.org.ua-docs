Додати повідомлення до хешу

-   [« sodium\_crypto\_generichash\_keygen](function.sodium-crypto-generichash-keygen.html)
    
-   [sodium\_crypto\_generichash »](function.sodium-crypto-generichash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Додати повідомлення до хешу
    

# sodiumcryptogenerichashupdate

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptogenerichashupdate — Додати повідомлення до хешу

### Опис

```methodsynopsis
sodium_crypto_generichash_update(string &$state, string $message): bool
```

Додає повідомлення до внутрішнього хеш-стану.

### Список параметрів

`state`

Значення, що повертається [sodium\_crypto\_generichash\_init()](function.sodium-crypto-generichash-init.html)

`message`

Дані для додавання до стану хешування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptogenerichashupdate()****

```php
<?php
$messages = [random_bytes(32), random_bytes(32), random_bytes(16)];
$state = sodium_crypto_generichash_init();
foreach ($messages as $message) {
    sodium_crypto_generichash_update($state, $message);
}
$final = sodium_crypto_generichash_final($state);
var_dump(sodium_bin2hex($final));

$allAtOnce = sodium_crypto_generichash(implode('', $messages));
var_dump(sodium_bin2hex($allAtOnce));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(64) "e16e28bbbbcc39d9f5b1cbc33c41f1d217808640103e57a41f24870f79831e04"
string(64) "e16e28bbbbcc39d9f5b1cbc33c41f1d217808640103e57a41f24870f79831e04"
```