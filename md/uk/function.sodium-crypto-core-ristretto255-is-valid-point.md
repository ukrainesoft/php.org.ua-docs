Визначає, чи лежить точка на кривій.

-   [« sodium\_crypto\_core\_ristretto255\_from\_hash](function.sodium-crypto-core-ristretto255-from-hash.html)
    
-   [sodium\_crypto\_core\_ristretto255\_random »](function.sodium-crypto-core-ristretto255-random.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Визначає, чи лежить точка на кривій.
    

# sodiumcryptocoreristretto255ісvalidpoint

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255ісvalidpoint — Визначає, чи лежить точка на кривій ristretto255

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_is_valid_point(string $s): bool
```

Визначає, чи лежить точка на кривій ristretto255 у канонічній формі на головній підгрупі і що точка не має малого порядку. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`s`

Крапка еліптичної кривої.

### Значення, що повертаються

Повертає **`true`**, якщо точка `s` знаходиться на кривій ristretto255, інакше повертає\*\*`false`

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255ісvalidpoint()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_scalarmult_ristretto255_base($foo);

var_dump(sodium_crypto_core_ristretto255_is_valid_point($bar));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.html) - Генерує випадковий ключ
-   [sodium\_crypto\_scalarmult\_ristretto255\_base()](function.sodium-crypto-scalarmult-ristretto255-base.html) - Обчислює відкритий ключ із закритого ключа