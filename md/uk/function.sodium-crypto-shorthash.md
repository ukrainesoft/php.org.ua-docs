Обчислює короткий хеш повідомлення та ключ

-   [« sodium\_crypto\_shorthash\_keygen](function.sodium-crypto-shorthash-keygen.html)
    
-   [sodium\_crypto\_sign\_detached »](function.sodium-crypto-sign-detached.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
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