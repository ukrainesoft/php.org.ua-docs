Отримати ASCII-кодований хеш

-   [« sodiumcryptopwhashstrverify](function.sodium-crypto-pwhash-str-verify.html)
    
-   [sodiumcryptopwhash »](function.sodium-crypto-pwhash.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   Отримати ASCII-кодований хеш
    

# sodiumcryptopwhashstr

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptopwhashstr — Отримати ASCII-кодований хеш

### Опис

```methodsynopsis
sodium_crypto_pwhash_str(string $password, int $opslimit, int $memlimit): string
```

Використовує ресурсомісткий за ЦПУ та пам'яті алгоритм хешування. Сіль генерується випадково. Можна встановити обмеження щодо використання пам'яті та ЦПУ. Можна використовувати для генерації ASCII-хешів, що підходять для зберігання паролів.

### Список параметрів

`password`

string; Пароль, для якого буде генеруватися хеш.

`opslimit`

Задає обмеження використання процесорного часу. Чим більше число - тим більше навантаження на процесор при генерації ключа. Також можна використовувати визначені константи для цього параметра (перераховані в порядку посилення захищеності та споживання ЦПУ): **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`** і **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**

`memlimit`

Задає обмеження використання пам'яті в байтах. Можна використовувати певні константи для цього параметра (перераховані в порядку посилення захищеності та споживання пам'яті): **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`** і **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**. Має сенс використовувати однакові рівні захищеності в memlimit та opslimit.

### Значення, що повертаються

Повертає хеш пароля.

Для того, щоб для того самого пароля завжди генерувався один і той же хеш, необхідно використовувати однакові значення `opslimit` і `memlimit`. Так як ці параметри включені в хеш, що згенерував, функція [sodiumcryptopwhashstrverify()](function.sodium-crypto-pwhash-str-verify.html) може перевіряти його коректність без необхідності зберігати ці параметри окремо.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptopwhashstr()****

```php
<?php
$password = 'password';
echo sodium_crypto_pwhash_str(
    $password,
    SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE,
    SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE
);
```

Результатом виконання цього прикладу буде щось подібне:

```
$argon2id$v=19$m=65536,t=2,p=1$oWIfdaXwWwhVmovOBc2NAQ$EbsZ+JnZyyavkafS0hoc4HdaOB0ILWZESAZ7kVGa+Iw
```

### Примітки

> **Зауваження**
> 
> Хеші обчислюються за допомогою алгоритму Argon2ID, стійкого для атак стороннього каналу та GPU. На відміну від функції [passwordhash()](function.password-hash.html), ця функція не має параметра salt (він генерується автоматично), а параметри `opslimit` і `memlimit` є обов'язковими.

### Дивіться також

-   [sodiumcryptopwhashstrverify()](function.sodium-crypto-pwhash-str-verify.html) - Перевіряє, що пароль відповідає хешу
-   [sodiumcryptopwhash()](function.sodium-crypto-pwhash.html) - Отримує ключ із пароля, використовуючи Argon2
-   [passwordhash()](function.password-hash.html) - Створює хеш пароля
-   [passwordverify()](function.password-verify.html) - Перевіряє, чи пароль хешу відповідає
-   [» Документация на Libsodium Argon2](https://download.libsodium.org/doc/password_hashing/the_argon2i_function.html)