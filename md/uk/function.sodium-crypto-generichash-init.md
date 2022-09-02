---
navigation:
  - function.sodium-crypto-generichash-final.md: « sodiumcryptogenerichashfinal
  - function.sodium-crypto-generichash-keygen.md: sodiumcryptogenerichashkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptogenerichashinit
---
# sodiumcryptogenerichashinit

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptogenerichashinit - Ініціалізує хеш для потокової передачі

### Опис

```methodsynopsis
sodium_crypto_generichash_init(string $key = "", int $length = SODIUM_CRYPTO_GENERICHASH_BYTES): string
```

Метод ініціалізації для потокового інтерфейсу API generichash.

### Список параметрів

`key`

Ключ generichash.

`length`

Очікувана довжина виведення хеш-функції.

### Значення, що повертаються

Повертає стан хешу, серіалізований як необроблений двійковий рядок.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptogenerichashinit()****

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
