---
navigation:
  - function.mcrypt-module-get-algo-key-size.md: « mcrypt\_module\_get\_algo\_key\_size
  - function.mcrypt-module-is-block-algorithm-mode.md: mcrypt\_module\_is\_block\_algorithm\_mode »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_get\_supported\_key\_sizes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_get\_supported\_key\_sizes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_get\_supported\_key\_sizes — Повертає список підтримуваних розмірів ключів для відкритого алгоритму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_supported_key_sizes(string $algorithm, string $lib_dir = ?): array
```

Повертає список підтримуваних розмірів ключів для відкритого алгоритму. Якщо повернутий порожній масив, то підтримується будь-яка довжина ключа від 1 до значення, що повертається. [mcrypt\_module\_get\_algo\_key\_size()](function.mcrypt-module-get-algo-key-size.md)

### Список параметрів

`algorithm`

Використовуваний алгоритм.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Повертає список підтримуваних розмірів ключів для відкритого алгоритму. Якщо повернутий порожній масив, то підтримується будь-яка довжина ключа від 1 до значення, що повертається. [mcrypt\_module\_get\_algo\_key\_size()](function.mcrypt-module-get-algo-key-size.md)

### Дивіться також

-   [mcrypt\_enc\_get\_supported\_key\_sizes()](function.mcrypt-enc-get-supported-key-sizes.md) \- Повертає масив з допустимими розмірами ключа для алгоритму
