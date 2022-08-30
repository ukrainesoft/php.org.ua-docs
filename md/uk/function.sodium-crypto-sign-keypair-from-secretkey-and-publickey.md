Об'єднує секретний ключ та відкритий ключ разом

-   [« sodiumcryptosigned25519сктоcurve25519](function.sodium-crypto-sign-ed25519-sk-to-curve25519.html)
    
-   [sodiumcryptosignkeypair »](function.sodium-crypto-sign-keypair.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Об'єднує секретний ключ та відкритий ключ разом
    

# sodiumcryptosignkeypairfromsecretkeyandpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignkeypairfromsecretkeyandpublickey — Об'єднує секретний ключ та відкритий ключ разом

### Опис

```methodsynopsis
sodium_crypto_sign_keypair_from_secretkey_and_publickey(string $secret_key, string $public_key): string
```

Об'єднує секретний ключ та відкритий ключ разом.

### Список параметрів

`secret_key`

Секретний ключ Ed25519

`public_key`

Відкритий ключ Ed25519

### Значення, що повертаються

Ключова пара