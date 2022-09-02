---
navigation:
  - function.mcrypt-enc-get-algorithms-name.md: « mcryptencgetalgorithmsname
  - function.mcrypt-enc-get-iv-size.md: mcryptencgetвербsize »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptencgetblocksize
---
# mcryptencgetblocksize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencgetblocksize — Повертає розмір блоку алгоритму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

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
