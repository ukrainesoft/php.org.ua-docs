Обчислює ключі сесії на стороні сервера

-   [« sodiumcryptoкксseedkeypair](function.sodium-crypto-kx-seed-keypair.html)
    
-   [sodiumcryptopwhashscryptsalsa208sha256strverify »](function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Обчислює ключі сесії на стороні сервера
    

# sodiumcryptoкксserversessionkeys

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксserversessionkeys — обчислює ключі сесії на стороні сервера

### Опис

```methodsynopsis
sodium_crypto_kx_server_session_keys(string $server_key_pair, string $client_key): array
```

Обчислює ключі сесії на стороні сервера за допомогою методу обміну ключами X25519 + BLAKE2b.

### Список параметрів

`server_key_pair`

Пара ключів cryptokx, наприклад, згенерована [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.html)

`client_key`

Відкритий ключ cryptokx.

### Значення, що повертаються

Масив, що складається із двох рядків. Першу слід використовуватиме отримання даних від клієнта. Другу слід використовувати для надсилання даних клієнту.