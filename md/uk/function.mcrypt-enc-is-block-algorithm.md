---
navigation:
  - function.mcrypt-enc-is-block-algorithm-mode.md: « mcrypt\_enc\_is\_block\_algorithm\_mode
  - function.mcrypt-enc-is-block-mode.md: mcrypt\_enc\_is\_block\_mode »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_is\_block\_algorithm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_is\_block\_algorithm

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_is\_block\_algorithm - Перевіряє, чи використовує алгоритм блокові режими

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_is_block_algorithm(resource $td): bool
```

Перевіряє, чи використовує алгоритм блокові режими.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо алгоритм є блоковим або \*\*`false`\*\*якщо потоковий.
