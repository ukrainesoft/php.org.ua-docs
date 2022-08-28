Отримати хеш повідомлення

-   [« sodium\_crypto\_generichash\_update](function.sodium-crypto-generichash-update.html)
    
-   [sodium\_crypto\_kdf\_derive\_from\_key »](function.sodium-crypto-kdf-derive-from-key.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Отримати хеш повідомлення
    

# sodiumcryptogenerichash

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptogenerichash — Отримати повідомлення хеша

### Опис

```methodsynopsis
sodium_crypto_generichash(string $message, string $key = "", int $length = SODIUM_CRYPTO_GENERICHASH_BYTES): string
```

Хешує повідомлення за допомогою BLAKE2b.

### Список параметрів

`message`

Хешені повідомлення.

`key`

(Необов'язковий) криптографічний ключ. Він виконує ту ж функцію, що й ключ HMAC, але використовується як зарезервований розділ внутрішнього стану BLAKE2.

`length`

Розмір виводу.

### Значення, що повертаються

Криптографічний хеш як необроблених байтів. Якщо бажаний висновок у шістнадцятковому коді, результат можна передати в [sodium\_bin2hex()](function.sodium-bin2hex.html)