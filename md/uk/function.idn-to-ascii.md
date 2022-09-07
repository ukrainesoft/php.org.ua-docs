---
navigation:
  - ref.intl.idn.md: « Функції IDN
  - function.idn-to-utf8.md: idnтоutf8 »
  - index.md: PHP Manual
  - ref.intl.idn.md: Функції IDN
title: idnтоascii
---
# idnтоascii

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.2, PECL idn >= 0.1)

idnтоascii — Перетворити доменне ім'я на формат IDNA ASCII

### Опис

Процедурний стиль

```methodsynopsis
idn_to_ascii(    string $domain,    int $flags = IDNA_DEFAULT,    int $variant = INTL_IDNA_VARIANT_UTS46,    array &$idna_info = null): string|false
```

Ця функція перетворює доменне ім'я з Unicode на IDNA ASCII.

### Список параметрів

`domain`

Ім'я для перетворення має бути в кодуванні UTF-8.

`flags`

Опції перетворення - комбінація констант IDNA (крім констант IDNAERROR

`variant`

**`INTL_IDNA_VARIANT_2003`** (оголошена застарілою починаючи з PHP 7.2.0) для IDNA 2003 або **`INTL_IDNA_VARIANT_UTS46`** (доступно лише з ICU 4.6) для UTS #46.

`idna_info`

Цей параметр використовується лише якщо використовується **`INTL_IDNA_VARIANT_UTS46`** в `variant`. У цьому випадку він буде заповнений масивом із ключами `'result'`, можливими помилковими результатами перетворення, `'isTransitionalDifferent'`, логічне вираз означає змінило або могло б змінити результат при використанні наскрізного механізму UTS #46, та `'errors'`, що містять ціле уявлення бітової маски з констант IDNAERROR

### Значення, що повертаються

Доменне ім'я у поданні ASCII або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер значення за замовчуванням `variant` змінено на **`INTL_IDNA_VARIANT_UTS46`** замість застарілої константи **`INTL_IDNA_VARIANT_2003`** |
|  | **`INTL_IDNA_VARIANT_2003`** оголошено застарілою, замість неї використовуйте **`INTL_IDNA_VARIANT_UTS46`** |

### Приклади

**Приклад #1 Приклад використання **idnтоascii()****

```php
<?php

echo idn_to_ascii('täst.de');

?>
```

Результат виконання цього прикладу:

```
xn--tst-qla.de
```

### Дивіться також

-   [idnтоutf8()](function.idn-to-utf8.md) - Перетворення доменного імені з IDNA ASCII в Unicode
