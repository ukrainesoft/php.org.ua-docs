---
navigation:
  - function.mcrypt-enc-get-block-size.md: « mcrypt\_enc\_get\_block\_size
  - function.mcrypt-enc-get-key-size.md: mcrypt\_enc\_get\_key\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_get\_iv\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_get\_iv\_size

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_get\_iv\_size — Повертає розмір вектора, що ініціалізує, для алгоритму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_iv_size(resource $td): int
```

Ця функція повертає розмір вектора, що ініціалізує, в байтах для алгоритму, заданого дескриптором шифрування. Ініціалізуючий вектор використовується в режимах cbc, cfb і ofb і деяких алгоритмах в потоковому режимі.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає розмір вектора, що ініціалізує, для алгоритму, або 0, якщо в цільовому алгоритмі він не використовується.
