Отримує ключ із пароля, використовуючи Argon2

-   [« sodiumcryptopwhashstr](function.sodium-crypto-pwhash-str.html)
    
-   [sodiumcryptoscalarmultbase »](function.sodium-crypto-scalarmult-base.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Отримує ключ із пароля, використовуючи Argon2
    

# sodiumcryptopwhash

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptopwhash — Отримує ключ із пароля, використовуючи Argon2

### Опис

```methodsynopsis
sodium_crypto_pwhash(    int $length,    string $password,    string $salt,    int $opslimit,    int $memlimit,    int $algo = SODIUM_CRYPTO_PWHASH_ALG_DEFAULT): string
```

Ця функція надає низькорівневий доступ до функції cryptopwhash бібліотеки libsodium. Якщо у вас немає принципової необхідності в цій функції, краще використовувати [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.html) або [passwordhash()](function.password-hash.html)

Найпоширеніша причина використання цієї конкретної функції - отримати початкові числа для криптографічних ключів з пароля та солі, а потім використовувати ці початкові числа для генерації фактичних ключів, необхідних для деяких цілей (наприклад, [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.html)

### Список параметрів

`length`

int; Довжина хешу пароля в байтах.

`password`

string; Пароль, для якого створюється хеш.

`salt`

Сіль, яку потрібно додати до пароля перед хешуванням. Сіль повинна бути непередбачуваною, в ідеалі, що генерується з хорошого джерела випадкових чисел, такого як [randombytes()](function.random-bytes.html), а також бути довжиною не менше байт, зазначених у константі **`SODIUM_CRYPTO_PWHASH_SALTBYTES`**

`opslimit`

Збільшення цього числа призведе до того, що функції знадобиться більше циклів ЦП для обчислення ключа. Існують константи, доступні для встановлення межі операцій для відповідних значень залежно від передбачуваного використання, у порядку зменшення: **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`** і **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**

`memlimit`

Максимальний обсяг ОЗП в байтах, який використовуватиме функція. Існують константи, які допоможуть вам вибрати відповідне значення як розмір: **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`** і **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**. Як правило, вони повинні поєднуватись з відповідними значеннями `opslimit`

`algo`

int Число, що вказує алгоритм хешування, що використовується. За замовчуванням задано **`SODIUM_CRYPTO_PWHASH_ALG_DEFAULT`** (рекомендований в даний час алгоритм, який може бути змінений при зміні версії libsodium на іншу), або явно використовуючи константу **`SODIUM_CRYPTO_PWHASH_ALG_ARGON2ID13`**, Що представляє версію алгоритму Argon2id 1.3

### Значення, що повертаються

Повертає пароль для захешування. Значення, що повертається, є бінарним рядком, а не ASCII-поданням і не містить ніякої додаткової інформації про параметри, з якими генерувався хеш. Таким чином, вам необхідно самим зберігати значення використаних параметрів для перевірки коректності хешу в майбутньому. Щоб усім цим не займатися – використовуйте функцію [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.html)

### Приклади

**Приклад #1 Приклад використання [passwordhash()](function.password-hash.html)**

```php
<?php
//Для дальнейшенй проверки необходимо сохранить соль
$salt = random_bytes(SODIUM_CRYPTO_PWHASH_SALTBYTES);
// Используем bin2hex для удобочитаемости
echo bin2hex(
    sodium_crypto_pwhash(
        16, // == 128 бит
        'password',
        $salt,
        SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE,
        SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE,
        SODIUM_CRYPTO_PWHASH_ALG_ARGON2ID13
    )
);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
a18f346ba57992eb7e4ae6abf3fd30ee
```