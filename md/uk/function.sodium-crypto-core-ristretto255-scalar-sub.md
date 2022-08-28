Віднімає скалярне значення

-   [« sodium\_crypto\_core\_ristretto255\_scalar\_reduce](function.sodium-crypto-core-ristretto255-scalar-reduce.html)
    
-   [sodium\_crypto\_core\_ristretto255\_sub »](function.sodium-crypto-core-ristretto255-sub.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Віднімає скалярне значення
    

# sodiumcryptocoreristretto255scalarsub

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarsub — Віднімає скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_sub(string $x, string $y): string
```

Віднімає скалярне значення `y` з `x`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255scalarsub()****

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

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.html) - Генерує випадковий ключ
-   [sodium\_crypto\_core\_ristretto255\_scalar\_add()](function.sodium-crypto-core-ristretto255-scalar-add.html) - Додає скалярне значення