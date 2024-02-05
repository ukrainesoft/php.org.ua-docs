---
navigation:
  - function.timezone-location-get.md: « timezone\_location\_get
  - function.timezone-name-get.md: timezone\_name\_get »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: timezone\_name\_from\_abbr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# timezone\_name\_from\_abbr

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

timezone\_name\_from\_abbr — Повертає назву часового поясу, вгадуючи абревіатуру та зміщення UTC

### Опис

```methodsynopsis
timezone_name_from_abbr(string $abbr, int $utcOffset = -1, int $isDST = -1): string|false
```

### Список параметрів

`abbr`

Абревіатура часового поясу.

`utcOffset`

Зміщення щодо GMT за секунди. За замовчуванням -1, що означає повернення першого знайденого часового поясу, що відповідає абревіатурі `abbr`. В іншому випадку буде здійснено пошук часового поясу із заданим усуненням. Якщо пошук завершиться невдачею, буде повернено найближчий часовий пояс.

`isDST`

Виправлення на літній час. За замовчуванням -1, у цьому випадку виправлення на літній час не враховується. Якщо передано 1, зсув `utcOffset` враховує діючий літній час. Якщо заданий 0, `utcOffset` розраховується з урахуванням зимового часу. Якщо `abbr` не існує, визначення часового поясу спирається тільки на `utcOffset`и`isDST`

### Значення, що повертаються

Возвращает имя часового пояса или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**timezone\_name\_from\_abbr()\*\*\*\*

```php
<?php
echo timezone_name_from_abbr("CET") . "\n";
echo timezone_name_from_abbr("", 3600, 0) . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Europe/Berlin
Europe/Paris
```

### Дивіться також

-   [timezone\_abbreviations\_list()](function.timezone-abbreviations-list.md) \- Псевдонім DateTimeZone::listAbbreviations
