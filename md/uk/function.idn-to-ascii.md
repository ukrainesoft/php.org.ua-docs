---
navigation:
  - ref.intl.idn.md: « Функції IDN
  - function.idn-to-utf8.md: idn\_to\_utf8 »
  - index.md: PHP Manual
  - ref.intl.idn.md: Функції IDN
title: idn\_to\_ascii
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# idn\_to\_ascii

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.2, PECL idn >= 0.1)

idn\_to\_ascii — Перетворює доменне ім'я на формат IDNA ASCII

### Опис

Процедурний стиль

```methodsynopsis
idn_to_ascii(    string $domain,    int $flags = IDNA_DEFAULT,    int $variant = INTL_IDNA_VARIANT_UTS46,    array &$idna_info = null): string|false
```

Ця функція перетворює доменне ім'я з Unicode на IDNA ASCII.

### Список параметрів

`domain`

Ім'я для перетворення має бути в кодуванні UTF-8.

`flags`

Опції перетворення – комбінація констант IDNA\_\*(кроме констант IDNA\_ERROR\_\*

`variant`

**`INTL_IDNA_VARIANT_2003`** (оголошена застарілою починаючи з PHP 7.2.0) для IDNA 2003 або **`INTL_IDNA_VARIANT_UTS46`** (доступно лише з ICU 4.6) для UTS #46.

`idna_info`

Цей параметр використовується лише якщо використовується \*\*`INTL_IDNA_VARIANT_UTS46`\*\*в`variant`. У цьому випадку він буде заповнений масивом із ключами `'result'`, можливими помилковими результатами перетворення, `'isTransitionalDifferent'`, логічне вираз означає змінило або могло б змінити результат при використанні наскрізного механізму UTS #46, та `'errors'`, що містять ціле уявлення бітової маски з констант IDNA\_ERROR\_\*

### Значення, що повертаються

Доменное имя в представлении ASCII или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Тепер значення за замовчуванням `variant`изменено на\*\*`INTL_IDNA_VARIANT_UTS46`\*\* замість застарілої константи **`INTL_IDNA_VARIANT_2003`** |
| 7.2.0 | **`INTL_IDNA_VARIANT_2003`** оголошено застарілою, замість неї використовуйте **`INTL_IDNA_VARIANT_UTS46`** |

### Приклади

**Приклад #1 Приклад використання** idn\_to\_ascii()\*\*\*\*

```php
<?php

echo idn_to_ascii('täst.de');

?>
```

Результат виконання наведеного прикладу:

```
xn--tst-qla.de
```

### Дивіться також

-   [idn\_to\_utf8()](function.idn-to-utf8.md) \- Перетворення доменного імені з IDNA ASCII в Unicode
