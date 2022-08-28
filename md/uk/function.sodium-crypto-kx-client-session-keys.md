Обчислює ключі сесії на стороні клієнта

-   [« sodium\_crypto\_kdf\_keygen](function.sodium-crypto-kdf-keygen.html)
    
-   [sodium\_crypto\_kx\_keypair »](function.sodium-crypto-kx-keypair.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Обчислює ключі сесії на стороні клієнта
    

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

Пара ключів cryptokx, наприклад, згенерована [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.html)

`server_key`

Відкритий ключ cryptokx.

### Значення, що повертаються

Масив, що складається із двох рядків. Першу слід використовувати для отримання даних із сервера. Другу слід використовувати для надсилання даних на сервер.