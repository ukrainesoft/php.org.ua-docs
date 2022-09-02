---
navigation:
  - function.sodium-crypto-scalarmult-ristretto255-base.md: « sodiumcryptoscalarmultristretto255base
  - function.sodium-crypto-scalarmult.md: sodiumcryptoscalarmult »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoscalarmultristretto255
---
# sodiumcryptoscalarmultristretto255

(PHP 8> = 8.1.1)

sodiumcryptoscalarmultristretto255 - Обчислює загальний секрет

### Опис

```methodsynopsis
sodium_crypto_scalarmult_ristretto255(string $n, string $p): string
```

Обчислює скаляр `n`, помножений на крапку `p`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`n`

Скаляр, який зазвичай є закритим ключем.

`p`

Крапка (x-координата), яка зазвичай є відкритим ключем.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodiumcryptoscalarmultristretto255base()](function.sodium-crypto-scalarmult-ristretto255-base.md) - Обчислює відкритий ключ із закритого ключа
