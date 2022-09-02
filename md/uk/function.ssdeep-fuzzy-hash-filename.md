---
navigation:
  - function.ssdeep-fuzzy-compare.md: « ssdeepfuzzycompare
  - function.ssdeep-fuzzy-hash.md: ssdeepfuzzyhash »
  - index.md: PHP Manual
  - ref.ssdeep.md: Функції ssdeep
title: ssdeepfuzzyhashfilename
---
# ssdeepfuzzyhashfilename

(PECL ssdeep >= 1.0.0)

ssdeepfuzzyhashfilename — Створення нечіткого хешу з файлу

### Опис

```methodsynopsis
ssdeep_fuzzy_hash_filename(string $file_name): string
```

**ssdeepfuzzyhashfilename()** обчислює хеш вказаного файлу `file_name`, використовуючи [» контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) та повертає його значення.

### Список параметрів

`file_name`

Ім'я файлу для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
