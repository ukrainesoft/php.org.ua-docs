---
navigation:
  - function.sodium-crypto-box-open.md: « sodiumcryptoboxopen
  - function.sodium-crypto-box-publickey.md: sodiumcryptoboxpublickey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoboxpublickeyfromsecretkey
---
# sodiumcryptoboxpublickeyfromsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxpublickeyfromsecretkey — Обчислює відкритий ключ із секретного ключа

### Опис

```methodsynopsis
sodium_crypto_box_publickey_from_secretkey(string $secret_key): string
```

З огляду на секретний ключ обчислює відповідний відкритий ключ.

Працює тільки з типом ключів, призначеним для використання з **cryptobox()** (який використовує еліптичну криву Діффі-Хеллмана на кривій Монтгомері, Curve25519; скорочено X25519), а не **cryptosign()** (який використовує алгоритм цифрового підпису Едвардса по кривій Едвардса з відповідними параметрами; скорочено Ed25519).

### Список параметрів

`secret_key`

Секретний ключ X25519

### Значення, що повертаються

Відкритий ключ X25519.
