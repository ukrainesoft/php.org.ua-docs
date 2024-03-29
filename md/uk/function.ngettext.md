---
navigation:
  - function.gettext.md: « gettext
  - function.textdomain.md: textdomain »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: ngettext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ngettext

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ngettext — Версія gettext для повідомлень у множині

### Опис

```methodsynopsis
ngettext(string $singular, string $plural, int $count): string
```

Версія [gettext()](function.gettext.md) для повідомлень у множині. Деякі мови мають більше однієї форми повідомлення для різних значень кількості.

### Список параметрів

`singular`

Ідентифікатор повідомлення в однині.

`plural`

Ідентифікатор повідомлення у множині.

`count`

Число (наприклад, кількість елементів) для визначення, яку граматичну форму використовувати.

### Значення, що повертаються

Повертає коректну форму повідомлення у множині, що ідентифікуються за параметрами `singular`и`plural` для кількості `count`

### Приклади

**Приклад #1 Приклад використання** ngettext()\*\*\*\*

```php
<?php

setlocale(LC_ALL, 'ru_RU');
printf(ngettext("%d window", "%d windows", 21), 21); // 21 окно
printf(ngettext("%d window", "%d windows", 22), 22); // 22 окна
printf(ngettext("%d window", "%d windows", 25), 25); // 25 окон

?>
```
