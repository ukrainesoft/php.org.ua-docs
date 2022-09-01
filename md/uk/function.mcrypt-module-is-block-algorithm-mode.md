---
navigation:
  - function.mcrypt-module-get-supported-key-sizes.html: « mcryptmodulegetsupportedkeysizes
  - function.mcrypt-module-is-block-algorithm.html: mcryptmoduleісblockalgorithm »
  - index.html: PHP Manual
  - ref.mcrypt.html: Mcrypt
title: mcryptmoduleісblockalgorithmmode
---
# mcryptmoduleісblockalgorithmmode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmoduleісblockalgorithmmode — Перевіряє, чи заданий модуль є блоковим.

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_is_block_algorithm_mode(string $mode, string $lib_dir = ?): bool
```

Функція повертає \*\*`true`\*\*якщо режим використовується з блочними алгоритмами, інакше повертає **`false`**. (тобто **`false`** для потокових та **`true`** для cbc, cfb, ofb).

### Список параметрів

`mode`

Режим, який перевірятиметься.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Функція повертає \*\*`true`\*\*якщо режим використовується з блочними алгоритмами, інакше повертає **`false`**. (тобто **`false`** для потокових та **`true`** для cbc, cfb, ofb).
