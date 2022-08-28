Витягує секретний ключ із ключової пари cryptobox

-   [« sodium\_crypto\_box\_seal](function.sodium-crypto-box-seal.html)
    
-   [sodium\_crypto\_box\_seed\_keypair »](function.sodium-crypto-box-seed-keypair.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Витягує секретний ключ із ключової пари cryptobox
    

# sodiumcryptoboxsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxsecretkey — Витягує секретний ключ із ключової пари cryptobox

### Опис

```methodsynopsis
sodium_crypto_box_secretkey(string $key_pair): string
```

Отримує лише секретний ключ для цієї ключової пари.

### Список параметрів

`key_pair`

Пара ключів, створена, наприклад, [sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.html) або [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.html)

### Значення, що повертаються

Секретний ключ X25519.