---
navigation:
  - function.mcrypt-enc-get-algorithms-name.md: « mcrypt\_enc\_get\_algorithms\_name
  - function.mcrypt-enc-get-iv-size.md: mcrypt\_enc\_get\_iv\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_get\_block\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_get\_block\_size

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_get\_block\_size — Повертає розмір блоку алгоритму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_block_size(resource $td): int
```

Повертає розмір блоку алгоритму.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає розмір блоку алгоритму у байтах.
