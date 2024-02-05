---
navigation:
  - function.jdtogregorian.md: « jdtogregorian
  - function.jdtojulian.md: jdtojulian »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: jdtojewish
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# jdtojewish

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtojewish — Переказує кількість днів із юліанського календаря в дату за єврейським календарем

### Опис

```methodsynopsis
jdtojewish(int $julian_day, bool $hebrew = false, int $flags = 0): string
```

Переказує кількість днів із юліанського календаря на дату за єврейським календарем.

### Список параметрів

`julian_day`

Номер дня у юліанському літочисленні у вигляді цілого числа

`hebrew`

Якщо аргумент `hebrew`установлен в\*\*`true`\*\*, дату буде повернено у вигляді закодованого рядка ISO-8859-8 у єврейському форматі, заданому аргументом `flags`

`flags`

Бітова маска може складатися з: **`CAL_JEWISH_ADD_ALAFIM_GERESH`** **`CAL_JEWISH_ADD_ALAFIM`**и**`CAL_JEWISH_ADD_GERESHAYIM`**

### Значення, що повертаються

Єврейська дата у вигляді рядка формату "місяць/день/рік" або закодований рядок ISO-8859-8 дати на івриті відповідно до параметра `hebrew`

### Приклади

**Пример #1 Пример использования**jdtojewish()\*\*\*\*

```php
<?php
$jd = gregoriantojd(10, 8, 2002);
echo jdtojewish($jd, true), PHP_EOL,
     jdtojewish($jd, true, CAL_JEWISH_ADD_GERESHAYIM), PHP_EOL,
     jdtojewish($jd, true, CAL_JEWISH_ADD_ALAFIM), PHP_EOL,
     jdtojewish($jd, true,CAL_JEWISH_ADD_ALAFIM_GERESH), PHP_EOL;
?>
```

Результат виконання наведеного прикладу:

```
ב חשון התשסג
ב' חשון התשס"ג
ב חשון ה אלפים תשסג
ב חשון ה'תשסג
```

### Дивіться також

-   [jewishtojd()](function.jewishtojd.md) \- Переказує дату за єврейським календарем у число днів у юліанському літочисленні
-   [cal\_from\_jd()](function.cal-from-jd.md) \- Перетворює дату, задану в юліанському календарі, на дату вказаного календаря
