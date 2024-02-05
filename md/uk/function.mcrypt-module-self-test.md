---
navigation:
  - function.mcrypt-module-open.md: « mcrypt\_module\_open
  - function.mdecrypt-generic.md: mdecrypt\_generic »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_self\_test
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_self\_test

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_self\_test — Функція запускає самоперевірку вказаного модуля

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_self_test(string $algorithm, string $lib_dir = ?): bool
```

Ця функція запускає самоперевірку вказаного алгоритму.

### Список параметрів

`algorithm`

Одна из констант\*\*`MCRYPT_ciphername`\*\*или название алгоритма в виде строки.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Ця функція повертає **`true`** якщо самоперевірка завершилася успішно та **`false`**, якщо ні.

### Приклади

**Пример #1 Пример использования**mcrypt\_module\_self\_test()\*\*\*\*

```php
<?php
var_dump(mcrypt_module_self_test(MCRYPT_RIJNDAEL_128)) . "\n";
var_dump(mcrypt_module_self_test(MCRYPT_BOGUS_CYPHER));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```
