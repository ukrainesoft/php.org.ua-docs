---
navigation:
  - function.mcrypt-get-block-size.md: « mcrypt\_get\_block\_size
  - function.mcrypt-get-iv-size.md: mcrypt\_get\_iv\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_get\_cipher\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_get\_cipher\_name

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_get\_cipher\_name — Отримує ім'я вказаного шифру

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_cipher_name(int $cipher): string
```

```methodsynopsis
mcrypt_get_cipher_name(string $cipher): string
```

Функция**mcrypt\_get\_cipher\_name()** використовується для отримання вказаного шифру.

**mcrypt\_get\_cipher\_name()** бере номер шифру як аргумент (libmcrypt 2.2.x) або ім'я шифру (libmcrypt 2.4.x або вище) і повертає ім'я шифру або \*\*`false`\*\*якщо шифр відсутній.

### Список параметрів

`cipher`

Одна из констант\*\*`MCRYPT_ciphername`\*\*или название алгоритма в виде строки.

### Значення, що повертаються

Функция возвращает имя шифра или\*\*`false`\*\*якщо такого шифру немає.

### Приклади

**Приклад #1 Приклад використання** mcrypt\_get\_cipher\_name()\*\*\*\*

```php
<?php
   $cipher = MCRYPT_TripleDES;

   echo mcrypt_get_cipher_name($cipher);
?>
```

Результат виконання наведеного прикладу:

```
3DES
```
