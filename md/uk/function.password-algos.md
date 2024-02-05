---
navigation:
  - ref.password.md: « Функції хешування паролів
  - function.password-get-info.md: password\_get\_info »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: password\_algos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# password\_algos

(PHP 7 >= 7.4.0, PHP 8)

password\_algos — Отримує доступні ідентифікатори алгоритму хешування пароля

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

**Пример #1 Пример использования**password()\*\*\*\*

```php
<?php
print_r(password_algos());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => 2y
    [1] => argon2i
    [2] => argon2id
)
```
