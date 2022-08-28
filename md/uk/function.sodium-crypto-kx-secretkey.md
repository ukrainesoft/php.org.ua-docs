Витягує секретний ключ із пари ключів cryptoккс

-   [« sodium\_crypto\_kx\_publickey](function.sodium-crypto-kx-publickey.html)
    
-   [sodium\_crypto\_kx\_seed\_keypair »](function.sodium-crypto-kx-seed-keypair.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Витягує секретний ключ із пари ключів cryptoккс
    

# sodiumcryptoкксsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксsecretkey — Витягує секретний ключ із пари ключів cryptoккс

### Опис

```methodsynopsis
sodium_crypto_kx_secretkey(string $key_pair): string
```

Витягує секретний ключ із пари ключів cryptokx.

### Список параметрів

`key_pair`

Пара ключів X25519, наприклад, згенерована [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.html)

### Значення, що повертаються

Секретний ключ X25519.