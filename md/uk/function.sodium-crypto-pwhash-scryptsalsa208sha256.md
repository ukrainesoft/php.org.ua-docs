Отримує ключ із пароля, використовуючи scrypt

-   [« sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str](function.sodium-crypto-pwhash-scryptsalsa208sha256-str.html)
    
-   [sodium\_crypto\_pwhash\_str\_needs\_rehash »](function.sodium-crypto-pwhash-str-needs-rehash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Отримує ключ із пароля, використовуючи scrypt
    

# sodiumcryptopwhashscryptsalsa208sha256

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptopwhashscryptsalsa208sha256 — Отримує ключ із пароля, використовуючи scrypt

### Опис

```methodsynopsis
sodium_crypto_pwhash_scryptsalsa208sha256(    int $length,    string $password,    string $salt,    int $opslimit,    int $memlimit): string
```

Аналог функції scrypt [sodium\_crypto\_pwhash()](function.sodium-crypto-pwhash.html)

Найпоширеніша причина використання цієї конкретної функції – отримати початкові числа для криптографічних ключів з пароля та солі, а потім використовувати ці початкові числа для генерації фактичних ключів, необхідних для деяких цілей (наприклад, [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.html)

### Список параметрів

`length`

Довжина генерованого хеша пароля в байтах.

`password`

Пароль, для якого створюється хеш.

`salt`

Сіль, яку потрібно додати до пароля перед хешуванням. Сіль має бути непередбачуваною, в ідеалі згенерованою з гарного джерела випадкових чисел, такого як [random\_bytes()](function.random-bytes.html), і мати довжину не менше **`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_SALTBYTES`** байт.

`opslimit`

Надає максимальну кількість обчислень для виконання. Збільшення цього числа призведе до того, що функції знадобиться більше циклів ЦП для обчислення ключа. Доступні деякі константи для встановлення межі операцій на відповідні значення залежно від передбачуваного використання у порядку розміру: **`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_OPSLIMIT_INTERACTIVE`** і **`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_OPSLIMIT_SENSITIVE`**

`memlimit`

Максимальний обсяг ОЗП, який використовуватиме функція, в байтах. Існують константи, які допоможуть вам вибрати відповідне значення в порядку їхнього розміру: **`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_MEMLIMIT_INTERACTIVE`** and **`SODIUM_CRYPTO_PWHASH_SCRYPTSALSA208SHA256_MEMLIMIT_SENSITIVE`**. Зазвичай вони повинні поєднуватись з відповідними значеннями `opslimit`

### Значення, що повертаються

Рядок байтів бажаної довжини.