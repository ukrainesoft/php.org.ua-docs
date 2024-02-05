---
navigation:
  - function.mcrypt-module-get-supported-key-sizes.md: « mcrypt\_module\_get\_supported\_key\_sizes
  - function.mcrypt-module-is-block-algorithm.md: mcrypt\_module\_is\_block\_algorithm »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_is\_block\_algorithm\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_is\_block\_algorithm\_mode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_is\_block\_algorithm\_mode — Перевіряє, чи заданий модуль є блоковим.

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_is_block_algorithm_mode(string $mode, string $lib_dir = ?): bool
```

Функція повертає \*\*`true`\*\*якщо режим використовується з блочними алгоритмами, інакше повертає **`false`**. (тобто **`false`** для потокових та \*\*`true`\*\*для cbc, cfb, ofb).

### Список параметрів

`mode`

Режим, який перевірятиметься.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Функція повертає \*\*`true`\*\*якщо режим використовується з блочними алгоритмами, інакше повертає **`false`**. (тобто **`false`** для потокових та \*\*`true`\*\*для cbc, cfb, ofb).
