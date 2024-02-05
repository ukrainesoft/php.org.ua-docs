---
navigation:
  - function.password-hash.md: « password\_hash
  - function.password-verify.md: password\_verify »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: password\_needs\_rehash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# password\_needs\_rehash

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

password\_needs\_rehash — Перевіряє, чи зазначений хеш відповідає заданим опціям

### Опис

```methodsynopsis
password_needs_rehash(string $hash, string|int|null $algo, array $options = []): bool
```

Перевіряє, що зазначений хеш відповідає заданим опціям та заданому алгоритму. Якщо ні, то можна дійти невтішного висновку у тому, що хеш треба перестворити.

### Список параметрів

`hash`

Хеш, створений функцією [password\_hash()](function.password-hash.md)

`algo`

[Константа](password.constants.md), Що позначає алгоритм хешування пароля, що використовується.

`options`

Асоціативний масив із опціями. За документацією щодо підтримуваних опцій для кожного алгоритму зверніться до розділу [Константи алгоритмів хешування паролів](password.constants.md)

### Значення, що повертаються

Повертає **`true`**якщо пароль повинен бути перехешований з використанням алгоритму `algo`и опций`options`, или**`false`**, якщо ні.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Параметр`algo` тепер чекає рядок (string), але все ще приймає число (int) зворотної сумісності. |

### Приклади

**Приклад #1 Приклад використання** password\_needs\_rehash()\*\*\*\*

```php
<?php

$password = 'rasmuslerdorf';
$hash = '$2y$10$YCFsG6elYca568hBi2pZ0.3LDL5wjgxct1N8w/oLR/jfHsiQwCqTS';

$algorithm = PASSWORD_BCRYPT;
// Значение bcrypt-стоимости может измениться по мере роста производительности оборудования
$options = ['cost' => 12];

// Сравниваем сохранённый хеш с открытым паролем
if (password_verify($password, $hash)) {
    // Проверяем, не изменился ли алгоритм или параметры
    if (password_needs_rehash($hash, $algorithm, $options)) {
        // Если были изменения, перехешируем и заменяем старый хеш новым
        $newHash = password_hash($password, $algorithm, $options);

        // Обновляем запись пользователя новым $newHash
    }

    // Авторизуем пользователя
}
?>
```
