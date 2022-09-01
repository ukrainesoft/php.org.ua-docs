---
navigation:
  - function.sodium-crypto-box-keypair.html: « sodiumcryptoboxkeypair
  - function.sodium-crypto-box-publickey-from-secretkey.html: sodiumcryptoboxpublickeyfromsecretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoboxopen
---
# sodiumcryptoboxopen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxopen — Розшифровка відкритого ключа з автентифікацією

### Опис

```methodsynopsis
sodium_crypto_box_open(string $ciphertext, string $nonce, string $key_pair): string|false
```

Розшифровує повідомлення із використанням асиметричної криптографії (з відкритим ключем).

### Список параметрів

`ciphertext`

Зашифроване повідомлення, яке потрібно спробувати розшифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.html)

`key_pair`

Дивіться [sodiumcryptoboxkeypairfromsecretkeyandpublickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html). Повинна включати відкритий ключ відправника та секретний ключ одержувача.

### Значення, що повертаються

Повертає повідомлення у разі успішного виконання або **`false`** у разі виникнення помилки.
