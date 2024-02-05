---
navigation:
  - function.sodium-crypto-box-seed-keypair.md: « sodium\_crypto\_box\_seed\_keypair
  - function.sodium-crypto-core-ristretto255-add.md: sodium\_crypto\_core\_ristretto255\_add »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box — Шифрування відкритим ключем із автентифікацією

### Опис

```methodsynopsis
sodium_crypto_box(string $message, string $nonce, string $key_pair): string
```

Шифрує повідомлення із використанням асиметричної криптографії (з відкритим ключем).

Алгоритм, що використовується функціями з префіксом **sodium\_crypto\_box()**: Еліптична крива Діффі-Хеллмана на кривій Монтгомері, Curve25519; зазвичай скорочено X25519.

### Список параметрів

`message`

Повідомлення, яке потрібно зашифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key_pair`

Смотрите[sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md). Повинен включати секретний ключ X25519 відправника та відкритий ключ X25519 одержувача.

### Значення, що повертаються

Повертає зашифроване повідомлення (зашифрований текст плюс тег аутентифікації). Зашифрований текст буде на 16 байтів довше, ніж відкритий текст, та необроблений двійковий рядок. Дивіться [sodium\_bin2base64()](function.sodium-bin2base64.md) для безпечного кодування для зберігання.
