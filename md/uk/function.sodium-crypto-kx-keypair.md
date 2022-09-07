---
navigation:
  - function.sodium-crypto-kx-client-session-keys.md: « sodiumcryptoкксclientsessionkeys
  - function.sodium-crypto-kx-publickey.md: sodiumcryptoкксpublickey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoкксkeypair
---
# sodiumcryptoкксkeypair

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксkeypair — Створює нову пару ключів.

### Опис

```methodsynopsis
sodium_crypto_kx_keypair(): string
```

Створити нову пару ключів sodium, що складається із секретного ключа (32 байти) і наступного за ним відкритого ключа (32 байти). Ключі можна отримати, викликавши [sodiumcryptoкксsecretkey()](function.sodium-crypto-kx-secretkey.md) і [sodiumcryptoкксpublickey()](function.sodium-crypto-kx-publickey.md) відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає нову пару ключів у разі успішного виконання; викидає виняток інакше.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptoкксkeypair()****

Створити нову пару ключів та витягти з неї секретний та відкритий ключі.

```php
<?php
$keypair = sodium_crypto_kx_keypair();
$secret = sodium_crypto_kx_secretkey($keypair);
$public = sodium_crypto_kx_publickey($keypair);
printf("секретный ключ: %s\nоткрытый ключ: %s", sodium_bin2hex($secret), sodium_bin2hex($public));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
секретный ключ: e7c5c918fdc40762e6000542c0118f4368ce8fd242b0e48c1e17202797a25daf
открытый ключ: d1f59fda8652caf40ed1a01d2b6f3802b60846986372cd8fa337b7c12c428b18
```
