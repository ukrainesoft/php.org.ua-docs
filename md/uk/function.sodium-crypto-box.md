---
navigation:
  - function.sodium-crypto-box-seed-keypair.md: « sodiumcryptoboxseedkeypair
  - function.sodium-crypto-core-ristretto255-add.md: sodiumcryptocoreristretto255add »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptobox
---
# sodiumcryptobox

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptobox — Шифрування відкритим ключем із автентифікацією

### Опис

```methodsynopsis
sodium_crypto_box(string $message, string $nonce, string $key_pair): string
```

Шифрує повідомлення із використанням асиметричної криптографії (з відкритим ключем).

Алгоритм, що використовується функціями з префіксом **sodiumcryptobox()**: Еліптична крива Діффі-Хеллмана на кривій Монтгомері, Curve25519; зазвичай скорочено X25519.

### Список параметрів

`message`

Повідомлення, яке потрібно зашифрувати.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.md)

`key_pair`

Дивіться [sodiumcryptoboxkeypairfromsecretkeyandpublickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md). Повинен включати секретний ключ X25519 відправника та відкритий ключ X25519 одержувача.

### Значення, що повертаються

Повертає зашифроване повідомлення (зашифрований текст плюс тег аутентифікації). Зашифрований текст буде на 16 байтів довше, ніж відкритий текст, та необроблений двійковий рядок. Дивіться [sodiumbin2base64()](function.sodium-bin2base64.md) для безпечного кодування для зберігання.
