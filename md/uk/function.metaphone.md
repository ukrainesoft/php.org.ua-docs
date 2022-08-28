Повертає ключ metaphone для рядка

-   [« md5](function.md5.html)
    
-   [money\_format »](function.money-format.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Повертає ключ metaphone для рядка
    

# metaphone

(PHP 4, PHP 5, PHP 7, PHP 8)

metaphone — Повертає ключ metaphone для рядка

### Опис

```methodsynopsis
metaphone(string $string, int $max_phonemes = 0): string
```

Повертає ключ metaphone для рядка `string`

Подібно до функції [soundex()](function.soundex.html), metaphone повертає однакове значення для слів, що мають подібну вимову. Ця функція точніша, ніж [soundex()](function.soundex.html), оскільки враховує основні правила вимови англійської. Довжина рядка, що повертається, не фіксована.

Функція metaphone була написана Lawrence Philips та описана в книзі "Practical Algorithms for Programmers", Binstock & Rex, Addison Wesley, 1995

### Список параметрів

`string`

Вхідний рядок.

`max_phonemes`

Цей параметр виставляє обмеження в `max_phonemes` *символів* на довжину ключа, що повертається metaphone. Однак результуючі фонеми завжди транскрибуються повністю, тому довжина результуючого рядка може бути трохи більшою, ніж `phonemes`. Значення за замовчуванням `0` означає відсутність обмежень.

### Значення, що повертаються

Повертає ключ metaphone у вигляді рядка.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція повертала **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Простий приклад використання **metaphone()****

```php
<?php
var_dump(metaphone('programming'));
var_dump(metaphone('programmer'));
?>
```

Результат виконання цього прикладу:

```
string(7) "PRKRMNK"
string(6) "PRKRMR"
```

**Приклад #2 Використання параметра `max_phonemes`**

```php
<?php
var_dump(metaphone('programming', 5));
var_dump(metaphone('programmer', 5));
?>
```

Результат виконання цього прикладу:

```
string(5) "PRKRM"
string(5) "PRKRM"
```

**Приклад #3 Використання параметра `max_phonemes`**

У цьому прикладі **metaphone()** пропонується створити рядок з п'яти символів, але для цього потрібно розділити останню фонему (`'x'` передбачається перетворити на `'KS'`), тому функція повертає рядок із шести символів.

```php
<?php
var_dump(metaphone('Asterix', 5));
?>
```

Результат виконання цього прикладу:

```
string(6) "ASTRKS"
```