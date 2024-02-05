---
navigation:
  - function.mcrypt-module-is-block-algorithm.md: « mcrypt\_module\_is\_block\_algorithm
  - function.mcrypt-module-open.md: mcrypt\_module\_open »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_is\_block\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_is\_block\_mode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_is\_block\_mode — Перевірити, чи вказаний режим повертає дані блоками.

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_is_block_mode(string $mode, string $lib_dir = ?): bool
```

Функція повертає **`true`**, якщо дані повертаються блоками та \*\*`false`\*\*якщо побайтно. (тобто **`true`** для cbc та ecb, та **`false`** для cfb та потоку).

### Список параметрів

`mode`

Одна из констант\*\*`MCRYPT_MODE_modename`\*\*, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Функція повертає **`true`**, якщо дані повертаються блоками та **`false`** якщо побайтно. (тобто **`true`** для cbc та ecb, та **`false`** для cfb та потоку).
