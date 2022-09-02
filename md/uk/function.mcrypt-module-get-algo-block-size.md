---
navigation:
  - function.mcrypt-module-close.md: « mcryptmoduleclose
  - function.mcrypt-module-get-algo-key-size.md: mcryptmodulegetalgokeysize »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptmodulegetalgoblocksize
---
# mcryptmodulegetalgoblocksize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmodulegetalgoblocksize — Повертає розмір блоку вказаного алгоритму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_algo_block_size(string $algorithm, string $lib_dir = ?): int
```

Повертає розмір блоку вказаного алгоритму.

### Список параметрів

`algorithm`

Ім'я алгоритму.

`lib_dir`

Опціональний параметр, у якому можна вказати директорію, що містить модуль режиму.

### Значення, що повертаються

Повертає розмір блоку вказаного алгоритму в байтах.
