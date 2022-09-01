---
navigation:
  - ref.password.md: « Функції хешування паролів
  - function.password-get-info.html: passwordgetinfo »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: passwordalgos
---
# passwordalgos

(PHP 7> = 7.4.0, PHP 8)

passwordalgos — Отримує доступні ідентифікатори алгоритму хешування пароля

### Опис

```methodsynopsis
password_algos(): array
```

Повертає повний список усіх зареєстрованих ідентифікаторів алгоритму хешування паролів у вигляді масиву (array) рядків (string)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає доступні ідентифікатори алгоритму хешування пароля.

### Приклади

**Приклад #1 Приклад використання **password()****

```php
<?php
print_r(password_algos());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => 2y
    [1] => argon2i
    [2] => argon2id
)
```
