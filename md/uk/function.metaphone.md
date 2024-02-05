---
navigation:
  - function.md5.md: « md5
  - function.money-format.md: money\_format »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: metaphone
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# metaphone

(PHP 4, PHP 5, PHP 7, PHP 8)

metaphone — Повертає ключ metaphone для рядка

### Опис

```methodsynopsis
metaphone(string $string, int $max_phonemes = 0): string
```

Повертає ключ metaphone для рядка `string`

Подібно до функції [soundex()](function.soundex.md), metaphone повертає однакове значення для слів, що мають подібну вимову. Ця функція точніша, ніж [soundex()](function.soundex.md), оскільки враховує основні правила вимови англійської. Довжина рядка, що повертається, не фіксована.

Функція metaphone була написана Lawrence Philips и описана в книге\["Practical Algorithms for Programmers", Binstock & Rex, Addison Wesley, 1995\]

### Список параметрів

`string`

Вхідний рядок.

`max_phonemes`

Цей параметр виставляє обмеження в `max_phonemes` *символів* на довжину ключа, що повертається metaphone. Однак результуючі фонеми завжди транскрибуються повністю, тому довжина результуючого рядка може бути трохи більшою, ніж `phonemes`Значение по умолчанию означает отсутствие ограничений.

### Значення, що повертаються

Повертає ключ metaphone у вигляді рядка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція повертала \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Простий приклад використання **metaphone()****

```php
<?php
var_dump(metaphone('programming'));
var_dump(metaphone('programmer'));
?>
```

Результат виконання наведеного прикладу:

```
string(7) "PRKRMNK"
string(6) "PRKRMR"
```

**Приклад #2 Использование параметра`max_phonemes`**

```php
<?php
var_dump(metaphone('programming', 5));
var_dump(metaphone('programmer', 5));
?>
```

Результат виконання наведеного прикладу:

```
string(5) "PRKRM"
string(5) "PRKRM"
```

**Приклад #3 Использование параметра`max_phonemes`**

У цьому прикладі **metaphone()** пропонується створити рядок з п'яти символів, але для цього потрібно розділити останню фонему (`'x'` передбачається перетворити на `'KS'`), тому функція повертає рядок із шести символів.

```php
<?php
var_dump(metaphone('Asterix', 5));
?>
```

Результат виконання наведеного прикладу:

```
string(6) "ASTRKS"
```
