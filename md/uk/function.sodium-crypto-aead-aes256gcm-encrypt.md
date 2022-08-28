Шифрує, а потім перевіряє справжність за допомогою AES-256-GCM

-   [« sodium\_crypto\_aead\_aes256gcm\_decrypt](function.sodium-crypto-aead-aes256gcm-decrypt.html)
    
-   [sodium\_crypto\_aead\_aes256gcm\_is\_available »](function.sodium-crypto-aead-aes256gcm-is-available.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Шифрує, а потім перевіряє справжність за допомогою AES-256-GCM
    

# sodiumcryptoaeadaes256gcmencrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmencrypt — Шифрує, а потім перевіряє справжність за допомогою AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_encrypt(    string $message,    string $additional_data,    string $nonce,    string $key): string
```

Шифрує, а потім перевіряє автентичність за допомогою AES-256-GCM. Доступно, тільки якщо [sodium\_crypto\_aead\_aes256gcm\_is\_available()](function.sodium-crypto-aead-aes256gcm-is-available.html) повертає **`true`**

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 12 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Повертає зашифрований текст і тег автентичності у вигляді рядка необроблених двійкових байтів. (Формат: зашифрований текст, потім тег.)