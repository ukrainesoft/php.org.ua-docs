---
navigation:
  - function.sodium-crypto-kx-seed-keypair.md: « sodium\_crypto\_kx\_seed\_keypair
  - function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.md: sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kx\_server\_session\_keys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kx\_server\_session\_keys

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kx\_server\_session\_keys — обчислює ключі сесії на стороні сервера

### Опис

```methodsynopsis
sodium_crypto_kx_server_session_keys(string $server_key_pair, string $client_key): array
```

Обчислює ключі сесії на стороні сервера за допомогою методу обміну ключами X25519 + BLAKE2b.

### Список параметрів

`server_key_pair`

Пара ключів crypto\_kx, наприклад, згенерована [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.md)

`client_key`

Відкритий ключ crypto\_kx.

### Значення, що повертаються

Масив, що складається із двох рядків. Першу слід використовуватиме отримання даних від клієнта. Другу слід використовувати для надсилання даних клієнту.
