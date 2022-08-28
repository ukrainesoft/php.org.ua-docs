Генерує випадковий ключ

-   [« sodium\_crypto\_core\_ristretto255\_scalar\_negate](function.sodium-crypto-core-ristretto255-scalar-negate.html)
    
-   [sodium\_crypto\_core\_ristretto255\_scalar\_reduce »](function.sodium-crypto-core-ristretto255-scalar-reduce.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Генерує випадковий ключ
    

# sodiumcryptocoreristretto255scalarrandom

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarrandom - Генерує випадковий ключ

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_random(): string
```

Генерує випадковий ключ. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255scalarrandom()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_core_ristretto255_scalar_random();

$value = sodium_crypto_core_ristretto255_scalar_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_scalar_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_add()](function.sodium-crypto-core-ristretto255-scalar-add.html) - Додає скалярне значення
-   [sodium\_crypto\_core\_ristretto255\_scalar\_sub()](function.sodium-crypto-core-ristretto255-scalar-sub.html) - Віднімає скалярне значення