---
navigation:
  - function.mcrypt-enc-get-supported-key-sizes.md: « mcrypt\_enc\_get\_supported\_key\_sizes
  - function.mcrypt-enc-is-block-algorithm.md: mcrypt\_enc\_is\_block\_algorithm »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_is\_block\_algorithm\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_is\_block\_algorithm\_mode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_is\_block\_algorithm\_mode — Перевіряє, чи використовується блоковий режим

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_is_block_algorithm_mode(resource $td): bool
```

Перевіряє, чи використовується блоковий режим (іншими словами, **`false`** для потоків та \*\*`true`\*\*для cbc, cfb, ofb)..

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`**, якщо використовується блоковий режим та **`false`**, якщо ні.
