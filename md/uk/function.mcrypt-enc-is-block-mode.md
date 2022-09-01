---
navigation:
  - function.mcrypt-enc-is-block-algorithm.html: « mcryptencісblockalgorithm
  - function.mcrypt-enc-self-test.html: mcryptencselftest »
  - index.html: PHP Manual
  - ref.mcrypt.html: Mcrypt
title: mcryptencісblockmode
---
# mcryptencісblockmode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencісblockmode — Перевіряє, чи поточний режим повертає блоки

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_is_block_mode(resource $td): bool
```

Перевіряє, чи поточний режим повертає блоки (тобто . **`true`** для cbc та ecb, та **`false`** для cfb та потоку).

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`**, якщо використовуваний режим повертає блоки та \*\*`false`\*\*якщо повертає байти.
