---
navigation:
  - function.mcrypt-module-get-algo-block-size.md: « mcrypt\_module\_get\_algo\_block\_size
  - function.mcrypt-module-get-supported-key-sizes.md: mcrypt\_module\_get\_supported\_key\_sizes »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_get\_algo\_key\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_get\_algo\_key\_size

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_get\_algo\_key\_size — Повернення максимального розміру ключа відкритого режиму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_algo_key_size(string $algorithm, string $lib_dir = ?): int
```

Повертає максимальний розмір ключа відкритого режиму.

### Список параметрів

`algorithm`

Ім'я алгоритму.

`lib_dir`

Опціональний параметр, де можна вказати директорію, що містить модуль режиму.

### Значення, що повертаються

Повертає максимальну довжину ключа у байтах для зазначеного алгоритму.
