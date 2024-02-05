---
navigation:
  - function.sodium-crypto-box-keypair.md: « sodium\_crypto\_box\_keypair
  - function.sodium-crypto-box-publickey-from-secretkey.md: sodium\_crypto\_box\_publickey\_from\_secretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_open

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_open — Розшифровка відкритого ключа з автентифікацією

### Опис

```methodsynopsis
sodium_crypto_box_open(string $ciphertext, string $nonce, string $key_pair): string|false
```

Розшифровує повідомлення із використанням асиметричної криптографії (з відкритим ключем).

### Список параметрів

`ciphertext`

Зашифроване повідомлення, яке потрібно спробувати розшифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key_pair`

Смотрите[sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md). Повинна включати відкритий ключ відправника та секретний ключ одержувача.

### Значення, що повертаються

Повертає повідомлення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
