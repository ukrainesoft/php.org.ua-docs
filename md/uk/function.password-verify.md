Перевіряє, чи пароль хешу відповідає

-   [« password\_needs\_rehash](function.password-needs-rehash.html)
    
-   [Sodium »](book.sodium.html)
    
-   [PHP Manual](index.html)
    
-   [Функции хеширования паролей](ref.password.html)
    
-   Перевіряє, чи пароль хешу відповідає
    

# passwordverify

(PHP 5> = 5.5.0, PHP 7, PHP 8)

passwordverify — Перевіряє, чи пароль хешу відповідає

### Опис

```methodsynopsis
password_verify(string $password, string $hash): bool
```

Перевіряє, чи пароль хешу відповідає. Функція **passwordverify()** сумісна з [crypt()](function.crypt.html). Отже, хеші паролів, створені [crypt()](function.crypt.html), можуть бути використані в **passwordverify()**

Зверніть увагу, що [password\_hash()](function.password-hash.html) повертає алгоритм, вартість та сіль як частини хешу. Таким чином, вся необхідна для перевірки інформація включена до нього. Це дозволяє проводити перевірку без необхідності зберігати всі ці дані окремо.

Ця функція безпечна для атак часу.

### Список параметрів

`password`

Користувальницький пароль.

`hash`

Хеш, створений функцією [password\_hash()](function.password-hash.html)

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

-   [password\_hash()](function.password-hash.html) - Створює хеш пароля
-   [» пользовательская реализация](https://github.com/ircmaxell/password_compat)
-   [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.html) - Перевіряє, що пароль відповідає хешу