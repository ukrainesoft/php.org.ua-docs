Розширює ключ та одноразовий номер у ключовий потік псевдовипадкових байтів

-   [« sodium\_crypto\_stream\_xchacha20\_xor](function.sodium-crypto-stream-xchacha20-xor.html)
    
-   [sodium\_crypto\_stream\_xor »](function.sodium-crypto-stream-xor.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Розширює ключ та одноразовий номер у ключовий потік псевдовипадкових байтів
    

# sodiumcryptostreamxchacha20

(PHP 8> = 8.1.0)

sodiumcryptostreamxchacha20 — Розширює ключ та одноразовий номер у ключовий потік псевдовипадкових байтів

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20(int $length, string $nonce, string $key): string
```

Розширює ключ `key` та одноразовий номер `nonce` у ключовий потік псевдовипадкових байтів.

### Список параметрів

`length`

Бажана кількість байтів.

`nonce`

24-байтовий одноразовий номер.

`key`

Ключ, можливо, згенерований за допомогою функції [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.html)

### Значення, що повертаються

Повертає псевдовипадковий потік, який можна використовувати функцією [sodium\_crypto\_stream\_xchacha20\_xor()](function.sodium-crypto-stream-xchacha20-xor.html)