---
navigation:
  - function.ssdeep-fuzzy-compare.md: « ssdeep\_fuzzy\_compare
  - function.ssdeep-fuzzy-hash.md: ssdeep\_fuzzy\_hash »
  - index.md: PHP Manual
  - ref.ssdeep.md: Функції ssdeep
title: ssdeep\_fuzzy\_hash\_filename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssdeep\_fuzzy\_hash\_filename

(PECL ssdeep >= 1.0.0)

ssdeep\_fuzzy\_hash\_filename — Створення нечіткого хешу з файлу

### Опис

```methodsynopsis
ssdeep_fuzzy_hash_filename(string $file_name): string
```

**ssdeep\_fuzzy\_hash\_filename()** обчислює хеш вказаного файлу `file_name`, используя[» контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) та повертає його значення.

### Список параметрів

`file_name`

Ім'я файлу для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
