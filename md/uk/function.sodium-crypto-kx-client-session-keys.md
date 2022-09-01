---
navigation:
  - function.sodium-crypto-kdf-keygen.html: « sodiumcryptokdfkeygen
  - function.sodium-crypto-kx-keypair.html: sodiumcryptoкксkeypair »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoкксclientsessionkeys
---
# sodiumcryptoкксclientsessionkeys

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксclientsessionkeys - обчислює ключі сесії на стороні клієнта

### Опис

```methodsynopsis
sodium_crypto_kx_client_session_keys(string $client_key_pair, string $server_key): array
```

Обчислює ключі сеансу на стороні клієнта за допомогою методу обміну ключами X25519 + BLAKE2b.

### Список параметрів

`client_key_pair`

Пара ключів cryptokx, наприклад, згенерована [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.html)

`server_key`

Відкритий ключ cryptokx.

### Значення, що повертаються

Масив, що складається із двох рядків. Першу слід використовувати для отримання даних із сервера. Другу слід використовувати для надсилання даних на сервер.
