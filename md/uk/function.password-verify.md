---
navigation:
  - function.password-needs-rehash.md: « password\_needs\_rehash
  - book.rnp.md: Rnp »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: password\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# password\_verify

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

password\_verify — Перевіряє, чи пароль хешу відповідає

### Опис

```methodsynopsis
password_verify(string $password, string $hash): bool
```

Перевіряє, чи пароль хешу відповідає. Функція \*\*password\_verify()\*\*совместима с[crypt()](function.crypt.md). Отже, хеші паролів, створені [crypt()](function.crypt.md), можуть бути використані в **password\_verify()**

Обратите внимание, что[password\_hash()](function.password-hash.md) повертає алгоритм, вартість та сіль як частини хешу. Таким чином, вся необхідна для перевірки інформація включена до нього. Це дозволяє проводити перевірку без необхідності зберігати всі ці дані окремо.

Ця функція безпечна для атак часу.

### Список параметрів

`password`

Користувальницький пароль.

`hash`

Хеш, створений функцією [password\_hash()](function.password-hash.md)

### Значення, що повертаються

Повертає **`true`** або **`false`**, Залежно від результатів перевірки.

### Приклади

**Приклад #1 Приклад використання** password\_verify()\*\*\*\*

Це спрощений приклад; за потреби рекомендується перестворити правильний пароль; дивіться приклад у описі функції [password\_needs\_rehash()](function.password-needs-rehash.md)

```php
<?php
// Смотрите Приклад использования password_hash(), для понимания откуда это взялось.
$hash = '$2y$10$.vGA1O9wmRjrwAVXD98HNOgsNpDczlqm3Jq7KnEd1rVAGv3Fykk1a';

if (password_verify('rasmuslerdorf', $hash)) {
    echo 'Пароль правильный!';
} else {
    echo 'Пароль неправильный.';
}
?>
```

Результат виконання наведеного прикладу:

```
Пароль правильный!
```

### Дивіться також

-   [password\_needs\_rehash()](function.password-needs-rehash.md) \- Перевіряє, що зазначений хеш відповідає заданим опціям
-   [password\_hash()](function.password-hash.md) \- Створює хеш пароля
-   [» користувацька реалізація](https://github.com/ircmaxell/password_compat)
-   [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.md) \- Перевіряє, що пароль відповідає хешу
