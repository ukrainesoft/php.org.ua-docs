Витягує відкритий ключ із ключової пари cryptobox

-   [« sodium\_crypto\_box\_publickey\_from\_secretkey](function.sodium-crypto-box-publickey-from-secretkey.html)
    
-   [sodium\_crypto\_box\_seal\_open »](function.sodium-crypto-box-seal-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Витягує відкритий ключ із ключової пари cryptobox
    

# sodiumcryptoboxpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxpublickey — Витягує відкритий ключ із ключової пари cryptobox

### Опис

```methodsynopsis
sodium_crypto_box_publickey(string $key_pair): string
```

Отримує лише відкритий ключ із ключової пари.

### Список параметрів

`key_pair`

Ключова пара, створена, наприклад, [sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.html) або [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.html)

### Значення, що повертаються

Відкритий ключ X25519.