---
navigation:
  - function.mcrypt-enc-get-iv-size.html: « mcryptencgetвербsize
  - function.mcrypt-enc-get-modes-name.html: mcryptencgetmodesname »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptencgetkeysize
---
# mcryptencgetkeysize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencgetkeysize — Повертає максимальну допустиму довжину ключа алгоритму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

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
