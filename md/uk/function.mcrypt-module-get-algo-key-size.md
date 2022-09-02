---
navigation:
  - function.mcrypt-module-get-algo-block-size.md: « mcryptmodulegetalgoblocksize
  - function.mcrypt-module-get-supported-key-sizes.md: mcryptmodulegetsupportedkeysizes »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptmodulegetalgokeysize
---
# mcryptmodulegetalgokeysize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmodulegetalgokeysize — Повернення максимального розміру ключа відкритого режиму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_algo_key_size(string $algorithm, string $lib_dir = ?): int
```

Повертає максимальний розмір ключа відкритого режиму.

### Список параметрів

`algorithm`

Ім'я алгоритму.

`lib_dir`

Опціональний параметр, у якому можна вказати директорію, що містить модуль режиму.

### Значення, що повертаються

Повертає максимальну довжину ключа у байтах для зазначеного алгоритму.
