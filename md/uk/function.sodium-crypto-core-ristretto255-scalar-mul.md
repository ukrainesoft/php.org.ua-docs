Помножує скалярне значення

-   [« sodium\_crypto\_core\_ristretto255\_scalar\_invert](function.sodium-crypto-core-ristretto255-scalar-invert.html)
    
-   [sodium\_crypto\_core\_ristretto255\_scalar\_negate »](function.sodium-crypto-core-ristretto255-scalar-negate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Помножує скалярне значення
    

# sodiumcryptocoreristretto255scalarmul

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarmul — Помножує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_mul(string $x, string $y): string
```

Помножує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.html) - Генерує випадковий ключ