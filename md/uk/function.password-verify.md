---
navigation:
  - function.password-needs-rehash.html: « passwordneedsrehash
  - book.sodium.html: Sodium »
  - index.html: PHP Manual
  - ref.password.html: Функції хешування паролів
title: passwordverify
---
# passwordverify

(PHP 5> = 5.5.0, PHP 7, PHP 8)

passwordverify — Перевіряє, чи пароль хешу відповідає

### Опис

```methodsynopsis
password_verify(string $password, string $hash): bool
```

Перевіряє, чи пароль хешу відповідає. Функція **passwordverify()** сумісна з [crypt()](function.crypt.html). Отже, хеші паролів, створені [crypt()](function.crypt.html), можуть бути використані в **passwordverify()**

Зверніть увагу, що [passwordhash()](function.password-hash.html) повертає алгоритм, вартість та сіль як частини хешу. Таким чином, вся необхідна для перевірки інформація включена до нього. Це дозволяє проводити перевірку без необхідності зберігати всі ці дані окремо.

Ця функція безпечна для атак часу.

### Список параметрів

`password`

Користувальницький пароль.

`hash`

Хеш, створений функцією [passwordhash()](function.password-hash.html)

### Значення, що повертаються

Повертає **`true`** або **`false`**, Залежно від результатів перевірки.

### Приклади

**Приклад #1 Приклад використання **passwordverify()****

```php
<?php
// Смотрите пример использования password_hash(), для понимания откуда это взялось.
$hash = '$2y$07$BCryptRequires22Chrcte/VlQH0piJtjXl.0t1XkA8pw9dMXTpOq';

if (password_verify('rasmuslerdorf', $hash)) {
    echo 'Пароль правильный!';
} else {
    echo 'Пароль неправильный.';
}
?>
```

Результат виконання цього прикладу:

```
Пароль правильный!
```

### Дивіться також

-   [passwordhash()](function.password-hash.html) - Створює хеш пароля
-   [» користувацька реалізація](https://github.com/ircmaxell/password_compat)
-   [sodiumcryptopwhashstrverify()](function.sodium-crypto-pwhash-str-verify.html) - Перевіряє, що пароль відповідає хешу
