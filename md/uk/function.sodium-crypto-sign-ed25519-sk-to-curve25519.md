Перетворити секретний ключ із системи Ed25519 на секретний ключ Curve25519

-   [« sodiumcryptosigned25519пктоcurve25519](function.sodium-crypto-sign-ed25519-pk-to-curve25519.html)
    
-   [sodiumcryptosignkeypairfromsecretkeyandpublickey »](function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перетворити секретний ключ із системи Ed25519 на секретний ключ Curve25519
    

# sodiumcryptosigned25519сктоcurve25519

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosigned25519сктоcurve25519 — Перетворити секретний ключ із системи Ed25519 на секретний ключ Curve25519

### Опис

```methodsynopsis
sodium_crypto_sign_ed25519_sk_to_curve25519(string $secret_key): string
```

Обчислює біраціонально-еквівалентний секретний ключ X25519 для секретного ключа Ed25519.

### Список параметрів

`secret_key`

Секретний ключ, що підходить для функцій cryptosign.

### Значення, що повертаються

Секретний ключ, що підходить для функцій cryptobox.