---
navigation:
  - function.ssdeep-fuzzy-hash-filename.md: « ssdeepfuzzyhashfilename
  - book.strings.md: Рядки »
  - index.md: PHP Manual
  - ref.ssdeep.md: Функції ssdeep
title: ssdeepfuzzyhash
---
# ssdeepfuzzyhash

(PECL ssdeep >= 1.0.0)

ssdeepfuzzyhash — Створює нечіткий хеш із рядка

### Опис

```methodsynopsis
ssdeep_fuzzy_hash(string $to_hash): string
```

**ssdeepfuzzyhash()** обчислює хеш рядки `to_hash`, використовуючи [»  контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) і повертає його.

### Список параметрів

`to_hash`

Рядок для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
