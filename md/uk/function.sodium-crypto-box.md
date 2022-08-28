Шифрування відкритим ключем з автентифікацією

-   [« sodium\_crypto\_box\_seed\_keypair](function.sodium-crypto-box-seed-keypair.html)
    
-   [sodium\_crypto\_core\_ristretto255\_add »](function.sodium-crypto-core-ristretto255-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Шифрування відкритим ключем з автентифікацією
    

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

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.html)

`key_pair`

Дивіться [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html). Повинен включати секретний ключ X25519 відправника та відкритий ключ X25519 одержувача.

### Значення, що повертаються

Повертає зашифроване повідомлення (зашифрований текст плюс тег аутентифікації). Зашифрований текст буде на 16 байтів довше, ніж відкритий текст, та необроблений двійковий рядок. Дивіться [sodium\_bin2base64()](function.sodium-bin2base64.html) для безпечного кодування для зберігання.