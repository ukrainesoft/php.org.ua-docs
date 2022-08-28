Витягує відкритий ключ із пари ключів cryptoккс

-   [« sodium\_crypto\_kx\_keypair](function.sodium-crypto-kx-keypair.html)
    
-   [sodium\_crypto\_kx\_secretkey »](function.sodium-crypto-kx-secretkey.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Витягує відкритий ключ із пари ключів cryptoккс
    

# sodiumcryptoкксpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксpublickey — Витягує відкритий ключ із пари ключів cryptoккс

### Опис

```methodsynopsis
sodium_crypto_kx_publickey(string $key_pair): string
```

Витягує відкритий ключ із пари ключів cryptokx.

### Список параметрів

`key_pair`

Пара ключів X25519, наприклад, згенерована [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.html)

### Значення, що повертаються

Відкритий ключ X25519.