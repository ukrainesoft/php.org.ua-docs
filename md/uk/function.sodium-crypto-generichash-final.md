Закінчити хешування

-   [« sodiumcryptocoreristretto255sub](function.sodium-crypto-core-ristretto255-sub.html)
    
-   [sodiumcryptogenerichashinit »](function.sodium-crypto-generichash-init.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Закінчити хешування
    

# sodiumcryptogenerichashfinal

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptogenerichashfinal - Закінчити хешування

### Опис

```methodsynopsis
sodium_crypto_generichash_final(string &$state, int $length = SODIUM_CRYPTO_GENERICHASH_BYTES): string
```

Метод завершення потокового API-інтерфейсу generichash.

### Список параметрів

`state`

Стан хешу, повернутий [sodiumcryptogenerichashinit()](function.sodium-crypto-generichash-init.html)

`length`

Довжина виведення.

### Значення, що повертаються

Криптографічний хеш.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptogenerichashfinal()****

```php
<?php
$messages = [random_bytes(32), random_bytes(32), random_bytes(16)];
$state = sodium_crypto_generichash_init('', 32);
foreach ($messages as $message) {
    sodium_crypto_generichash_update($state, $message);
}

$final = sodium_crypto_generichash_final($state, 32);
var_dump(sodium_bin2hex($final));

$allAtOnce = sodium_crypto_generichash(implode('', $messages));
var_dump(sodium_bin2hex($allAtOnce));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(64) "a2939a9163cb7c796ec28e01028489e72475c136b2697ea59e3e760ab4a8ab20"
string(64) "a2939a9163cb7c796ec28e01028489e72475c136b2697ea59e3e760ab4a8ab20"
```