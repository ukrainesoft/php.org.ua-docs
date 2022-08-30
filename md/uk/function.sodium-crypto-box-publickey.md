Витягує відкритий ключ із ключової пари cryptobox

-   [« sodiumcryptoboxpublickeyfromsecretkey](function.sodium-crypto-box-publickey-from-secretkey.html)
    
-   [sodiumcryptoboxsealopen »](function.sodium-crypto-box-seal-open.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
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

Ключова пара, створена, наприклад, [sodiumcryptoboxkeypair()](function.sodium-crypto-box-keypair.html) або [sodiumcryptoboxseedkeypair()](function.sodium-crypto-box-seed-keypair.html)

### Значення, що повертаються

Відкритий ключ X25519.