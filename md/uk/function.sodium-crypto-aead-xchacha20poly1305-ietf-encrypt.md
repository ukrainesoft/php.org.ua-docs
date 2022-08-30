(Переважно) Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305

-   [« sodiumcryptoaeadxchacha20poly1305ietfdecrypt](function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.html)
    
-   [sodiumcryptoaeadxchacha20poly1305ietfkeygen »](function.sodium-crypto-aead-xchacha20poly1305-ietf-keygen.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   (Переважно) Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305
    

# sodiumcryptoaeadxchacha20poly1305ietfencrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadxchacha20poly1305ietfencrypt — (Переважно) Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_encrypt(    string $message,    string $additional_data,    string $nonce,    string $key): string
```

Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305 (варіант eXtended-nonce).

Як правило, XChaCha20-Poly1305 - найкращий з наявних режимів AEAD для використання.

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.html)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає зашифрований текст та тег або **`false`** у разі виникнення помилки.