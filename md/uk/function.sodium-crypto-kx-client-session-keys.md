---
navigation:
  - function.sodium-crypto-kdf-keygen.md: « sodium\_crypto\_kdf\_keygen
  - function.sodium-crypto-kx-keypair.md: sodium\_crypto\_kx\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kx\_client\_session\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kx\_client\_session\_keys

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kx\_client\_session\_keys - обчислює ключі сесії на стороні клієнта

### Опис

```methodsynopsis
sodium_crypto_kx_client_session_keys(string $client_key_pair, string $server_key): array
```

Обчислює ключі сеансу на стороні клієнта за допомогою методу обміну ключами X25519 + BLAKE2b.

### Список параметрів

`client_key_pair`

Пара ключів crypto\_kx, наприклад, згенерована [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.md)

`server_key`

Відкритий ключ crypto\_kx.

### Значення, що повертаються

Масив, що складається із двох рядків. Першу слід використовувати для отримання даних із сервера. Другу слід використовувати для надсилання даних на сервер.
