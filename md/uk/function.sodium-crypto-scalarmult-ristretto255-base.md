Обчислює відкритий ключ із закритого ключа

-   [« sodiumcryptoscalarmultbase](function.sodium-crypto-scalarmult-base.html)
    
-   [sodiumcryptoscalarmultristretto255 »](function.sodium-crypto-scalarmult-ristretto255.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Обчислює відкритий ключ із закритого ключа
    

# sodiumcryptoscalarmultristretto255base

(PHP 8> = 8.1.1)

sodiumcryptoscalarmultristretto255base — Обчислює відкритий ключ із закритого ключа

### Опис

```methodsynopsis
sodium_crypto_scalarmult_ristretto255_base(string $n): string
```

З огляду на закритий ключ обчислює відповідний відкритий ключ. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`n`

Закритий ключ.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodiumcryptoscalarmultristretto255()](function.sodium-crypto-scalarmult-ristretto255.html) - обчислює загальний секрет