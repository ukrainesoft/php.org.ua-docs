Розшифровка відкритого ключа з автентифікацією

-   [« sodium\_crypto\_box\_keypair](function.sodium-crypto-box-keypair.html)
    
-   [sodium\_crypto\_box\_publickey\_from\_secretkey »](function.sodium-crypto-box-publickey-from-secretkey.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Розшифровка відкритого ключа з автентифікацією
    

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

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.html)

`key_pair`

Дивіться [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html). Повинна включати відкритий ключ відправника та секретний ключ одержувача.

### Значення, що повертаються

Повертає повідомлення у разі успішного виконання або **`false`** у разі виникнення помилки.