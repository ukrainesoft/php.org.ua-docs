---
navigation:
  - function.sodium-crypto-scalarmult-base.md: « sodiumcryptoscalarmultbase
  - function.sodium-crypto-scalarmult-ristretto255.md: sodiumcryptoscalarmultristretto255 »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoscalarmultristretto255base
---
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

-   [sodiumcryptoscalarmultristretto255()](function.sodium-crypto-scalarmult-ristretto255.md) - обчислює загальний секрет
