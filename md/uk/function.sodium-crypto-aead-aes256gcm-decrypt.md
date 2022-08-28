Перевіряє та розшифровує повідомлення за допомогою AES-256-GCM

-   [« sodium\_compare](function.sodium-compare.html)
    
-   [sodium\_crypto\_aead\_aes256gcm\_encrypt »](function.sodium-crypto-aead-aes256gcm-encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевіряє та розшифровує повідомлення за допомогою AES-256-GCM
    

# sodiumcryptoaeadaes256gcmdecrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmdecrypt — Перевірка та розшифрування повідомлення за допомогою AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

Перевіряє та розшифровує повідомлення за допомогою AES-256-GCM Доступно, лише якщо [sodium\_crypto\_aead\_aes256gcm\_is\_available()](function.sodium-crypto-aead-aes256gcm-is-available.html) повертає **`true`**

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodium\_crypto\_aead\_aes256gcm\_encrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.html) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується для перевірки тега автентифікації, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 12 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або **`false`** у разі виникнення помилки.