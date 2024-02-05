---
navigation:
  - function.mcrypt-enc-is-block-mode.md: « mcrypt\_enc\_is\_block\_mode
  - function.mcrypt-encrypt.md: mcrypt\_encrypt »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_self\_test
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_self\_test

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_self\_test — Запуск самоперевірки відкритого модуля

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_self_test(resource $td): int
```

Функція запускає самоперевірку алгоритму, заданого дескриптором шифрування `td`

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає у разі успішного виконання та негативне int в іншому випадку.
