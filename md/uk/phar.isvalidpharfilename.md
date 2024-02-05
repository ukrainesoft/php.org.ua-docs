---
navigation:
  - phar.isfileformat.md: '« Phar::isFileFormat'
  - phar.iswritable.md: 'Phar::isWritable »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::isValidPharFilename'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::isValidPharFilename

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

Phar::isValidPharFilename — Перевіряє, що задане ім'я файлу є коректним ім'ям phar-архіву

### Опис

```methodsynopsis
final public static Phar::isValidPharFilename(string $filename, bool $executable = true): bool
```

Перевіряє, що ім'я файлу є коректним ім'ям phar-архіву. Можна використовувати для перевірки імені файлу до моменту його безпосереднього створення, щоб уникнути небажаних винятків.

### Список параметрів

`filename`

Ім'я або повний шлях до файлу, який ще не створено

`executable`

Цей параметр визначає, чи повинен файл розпізнаватись як архів, що запускається, або як архів, що не запускається, з даними

### Значення, що повертаються

Повертає **`true`**или**`false`**
