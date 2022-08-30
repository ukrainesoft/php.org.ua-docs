Обчислює короткий хеш повідомлення та ключ

-   [« sodiumcryptoshorthashkeygen](function.sodium-crypto-shorthash-keygen.html)
    
-   [sodiumcryptosigndetached »](function.sodium-crypto-sign-detached.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   Обчислює короткий хеш повідомлення та ключ
    

# sodiumcryptoshorthash

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoshorthash — Обчислює короткий хеш повідомлення та ключ

### Опис

```methodsynopsis
sodium_crypto_shorthash(string $message, string $key): string
```

**sodiumcryptoshorthash()** обгортає хеш-функцію під назвою SipHash-2-4, яка ідеально підходить для реалізації хеш-таблиць, які не схильні до атак відмови в обслуговуванні через колізію хешів (Hash-DoS).

SipHash-2-4 не є криптографічною хеш-функцією загального призначення.

### Список параметрів

`message`

Повідомлення, хеш якого потрібно обчислити.

`key`

Хеш-ключ.

### Значення, що повертаються