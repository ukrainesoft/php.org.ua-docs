---
navigation:
  - function.mcrypt-enc-get-supported-key-sizes.html: « mcryptencgetsupportedkeysizes
  - function.mcrypt-enc-is-block-algorithm.html: mcryptencісblockalgorithm »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptencісblockalgorithmmode
---
# mcryptencісblockalgorithmmode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencісblockalgorithmmode — Перевіряє, чи використовується блоковий режим

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_is_block_algorithm_mode(resource $td): bool
```

Перевіряє, чи використовується блоковий режим (іншими словами, **`false`** для потоків та **`true`** для cbc, cfb, ofb).

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`**, якщо використовується блоковий режим та **`false`**, якщо ні.
