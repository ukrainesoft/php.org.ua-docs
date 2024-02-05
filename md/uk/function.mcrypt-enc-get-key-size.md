---
navigation:
  - function.mcrypt-enc-get-iv-size.md: « mcrypt\_enc\_get\_iv\_size
  - function.mcrypt-enc-get-modes-name.md: mcrypt\_enc\_get\_modes\_name »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_get\_key\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_get\_key\_size

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_get\_key\_size — Повертає максимальну допустиму довжину ключа алгоритму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_key_size(resource $td): int
```

Повертає максимальну допустиму довжину ключа алгоритму в байтах.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає максимальну допустиму довжину ключа алгоритму в байтах.
