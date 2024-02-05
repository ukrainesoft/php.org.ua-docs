---
navigation:
  - ref.ssdeep.md: « Функції ssdeep
  - function.ssdeep-fuzzy-hash-filename.md: ssdeep\_fuzzy\_hash\_filename »
  - index.md: PHP Manual
  - ref.ssdeep.md: Функції ssdeep
title: ssdeep\_fuzzy\_compare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssdeep\_fuzzy\_compare

(PECL ssdeep >= 1.0.0)

ssdeep\_fuzzy\_compare — Обчислює схожість двох сигнатур нечітких хешів

### Опис

```methodsynopsis
ssdeep_fuzzy_compare(string $signature1, string $signature2): int
```

Обчислює величину збігу між `signature1`и`signature2`, используя[»  контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) та повертає її.

### Список параметрів

`signature1`

Перший рядок із сигнатурою нечіткого хешування.

`signature2`

Другий рядок із сигнатурою нечіткого хешування.

### Значення, що повертаються

Повертає ціле число в діапазоні від 0 до 100 у разі успішного виконання або **`false`** в іншому випадку.
