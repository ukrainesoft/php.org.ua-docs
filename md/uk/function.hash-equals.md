---
navigation:
  - function.hash-copy.md: « hashcopy
  - function.hash-file.md: hashfile »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashequals
---
# hashequals

(PHP 5> = 5.6.0, PHP 7, PHP 8)

hashequals - Порівняння рядків, нечутливе до атак за часом

### Опис

```methodsynopsis
hash_equals(string $known_string, string $user_string): bool
```

Порівнює два рядки на ідентичність, використовуючи однаковий час незалежно від того, рівні вони чи ні.

Ця функція може використовуватися для запобігання атакам за часом; Наприклад при перевірці хешей паролів за допомогою [crypt()](function.crypt.md)

### Список параметрів

`known_string`

Рядок відомої довжини, з якою буде проводитись порівняння.

`user_string`

Перевірений рядок.

### Значення, що повертаються

Повертає **`true`** якщо рядки ідентичні та **`false`** якщо ні.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо один із параметрів не є рядком.

### Приклади

**Приклад #1 Приклад використання **hashequals()****

```php
<?php
$expected  = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$correct   = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$incorrect = crypt('apple', '$2a$07$usesomesillystringforsalt$');

var_dump(hash_equals($expected, $correct));
var_dump(hash_equals($expected, $incorrect));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Примітки

> **Зауваження**
> 
> Обидва аргументи мають бути однієї довжини. Якщо передано аргументи різної довжини, то буде негайно повернено **`false`**, і довжина відомого рядка може бути визначена у разі атаки за часом.

> **Зауваження**
> 
> Вкрай важливо ставити рядок з даними користувача другим аргументом, а не першим.
