Шифрує повідомлення без автентифікації

-   [« sodium\_crypto\_stream\_xchacha20](function.sodium-crypto-stream-xchacha20.html)
    
-   [sodium\_crypto\_stream »](function.sodium-crypto-stream.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Шифрує повідомлення без автентифікації
    

# sodiumcryptostreamxor

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptostreamxor — Шифрує повідомлення без автентифікації

### Опис

```methodsynopsis
sodium_crypto_stream_xor(string $message, string $nonce, string $key): string
```

Функція шифрує повідомлення за допомогою XSalsa20, але не надає жодної гарантії зашифрованого тексту для відкритого тексту.

### Список параметрів

`message`

Повідомлення для шифрування

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.html)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Зашифровані повідомлення.