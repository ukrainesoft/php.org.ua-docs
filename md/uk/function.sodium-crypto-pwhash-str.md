---
navigation:
  - function.sodium-crypto-pwhash-str-verify.md: « sodium\_crypto\_pwhash\_str\_verify
  - function.sodium-crypto-pwhash.md: sodium\_crypto\_pwhash »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_pwhash\_str
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_pwhash\_str

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_pwhash\_str — Отримати ASCII-кодований хеш

### Опис

```methodsynopsis
sodium_crypto_pwhash_str(string $password, int $opslimit, int $memlimit): string
```

Використовує ресурсомісткий за ЦПУ та пам'яті алгоритм хешування. Сіль генерується випадково. Можна встановити обмеження щодо використання пам'яті та ЦПУ. Можна використовувати для генерації ASCII-хешів, що підходять для зберігання паролів.

### Список параметрів

`password`

string; Пароль, для якого генеруватиметься хеш.

`opslimit`

Задає обмеження використання процесорного часу. Чим більше число - тим більше навантаження на процесор при генерації ключа. Також можна використовувати певні константи для цього параметра (перераховані у порядку посилення захищеності та споживання ЦПУ): **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`**и**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**

`memlimit`

Задає обмеження використання пам'яті в байтах. Можна використовувати певні константи для цього параметра (перераховані в порядку посилення захищеності та споживання пам'яті): **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`** **`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`**и**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**. Має сенс використовувати однакові рівні захищеності в memlimit та opslimit.

### Значення, що повертаються

Повертає хеш пароля.

Для того, щоб для того самого пароля завжди генерувався один і той же хеш, необхідно використовувати однакові значення `opslimit`и`memlimit`. Оскільки ці параметри включені в згенерований хеш, функція [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.md) може перевіряти його коректність без необхідності зберігати ці параметри окремо.

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_pwhash\_str()\*\*\*\*

```php
<?php
$password = 'password';
echo sodium_crypto_pwhash_str(
    $password,
    SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE,
    SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE
);
```

Висновок наведеного прикладу буде схожим на:

```
$argon2id$v=19$m=65536,t=2,p=1$oWIfdaXwWwhVmovOBc2NAQ$EbsZ+JnZyyavkafS0hoc4HdaOB0ILWZESAZ7kVGa+Iw
```

### Примітки

> **Зауваження** :
> 
> Хеші обчислюються за допомогою алгоритму Argon2ID, стійкого для атак стороннього каналу та GPU. На відміну від функції [password\_hash()](function.password-hash.md), ця функція не має параметра salt (він генерується автоматично), а параметри `opslimit`и`memlimit` є обов'язковими.

### Дивіться також

-   [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.md) \- Перевіряє, що пароль відповідає хешу
-   [sodium\_crypto\_pwhash()](function.sodium-crypto-pwhash.md) \- Отримує ключ із пароля, використовуючи Argon2
-   [password\_hash()](function.password-hash.md) \- Створює хеш пароля
-   [password\_verify()](function.password-verify.md) \- Перевіряє, чи пароль хешу відповідає
-   [» Документація на Libsodium Argon2](https://download.libsodium.org/doc/password_hashing/the_argon2i_function.md)
