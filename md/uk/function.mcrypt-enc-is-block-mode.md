---
navigation:
  - function.mcrypt-enc-is-block-algorithm.md: « mcrypt\_enc\_is\_block\_algorithm
  - function.mcrypt-enc-self-test.md: mcrypt\_enc\_self\_test »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_is\_block\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_is\_block\_mode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_is\_block\_mode — Перевіряє, чи поточний режим повертає блоки

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

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
