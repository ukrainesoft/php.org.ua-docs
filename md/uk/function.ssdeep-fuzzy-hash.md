---
navigation:
  - function.ssdeep-fuzzy-hash-filename.md: « ssdeep\_fuzzy\_hash\_filename
  - book.strings.md: Рядки »
  - index.md: PHP Manual
  - ref.ssdeep.md: Функції ssdeep
title: ssdeep\_fuzzy\_hash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssdeep\_fuzzy\_hash

(PECL ssdeep >= 1.0.0)

ssdeep\_fuzzy\_hash — Створює нечіткий хеш із рядка

### Опис

```methodsynopsis
ssdeep_fuzzy_hash(string $to_hash): string
```

**ssdeep\_fuzzy\_hash()** обчислює хеш рядки `to_hash`, используя[»  контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) і повертає його.

### Список параметрів

`to_hash`

Рядок для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
