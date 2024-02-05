---
navigation:
  - function.juliantojd.md: « juliantojd
  - book.datetime.md: Дата час "
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: unixtojd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# unixtojd

(PHP 4, PHP 5, PHP 7, PHP 8)

unixtojd — Перекладає мітку часу Unix у юліанський день

### Опис

```methodsynopsis
unixtojd(?int $timestamp = null): int|false
```

Повертає юліанський день для заданої позначки часу Unix `timestamp` (кількість секунд з 1.1.1970) або для поточного часу, якщо аргумент `timestamp` не заданий. У будь-якому випадку час розглядається як місцевий час (не UTC).

### Список параметрів

`timestamp`

Мітка часу Unix для перетворення.

### Значення, що повертаються

Число днів у юліанському літочисленні або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timestamp` тепер допускає значення null. |

### Дивіться також

-   [jdtounix()](function.jdtounix.md) \- Переказує кількість днів у юліанському літочисленні у мітку часу Unix
