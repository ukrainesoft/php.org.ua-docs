---
navigation:
  - function.sodium-crypto-auth.html: « sodiumcryptoauth
  - function.sodium-crypto-box-keypair.html: sodiumcryptoboxkeypair »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptoboxkeypairfromsecretkeyandpublickey
---
# sodiumcryptoboxkeypairfromsecretkeyandpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxkeypairfromsecretkeyandpublickey — Створює уніфікований рядок ключової пари із секретного та відкритого ключів

### Опис

```methodsynopsis
sodium_crypto_box_keypair_from_secretkey_and_publickey(string $secret_key, string $public_key): string
```

Функція існує для задоволення вимог API, наприклад **cryptobox()**. Передайте секретний ключ однієї сторони та відкритий ключ інший, і ви отримаєте ключову пару для комунікації.

### Список параметрів

`secret_key`

Секретний ключ.

`public_key`

Відкритий ключ.

### Значення, що повертаються

Ключова пара X25519.
