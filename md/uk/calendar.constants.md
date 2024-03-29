---
navigation:
  - calendar.resources.md: « Типи ресурсів
  - ref.calendar.md: Календар »
  - index.md: PHP Manual
  - book.calendar.md: Календар
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`CAL_EASTER_DEFAULT`**(int)

Для[easter\_days()](function.easter-days.md): обчислювати Великдень для років до 1753 за юліанським календарем, а в наступні роки за григоріанським календарем.

**`CAL_EASTER_ROMAN`**(int)

Для[easter\_days()](function.easter-days.md): обчислювати Великдень для років до 1583 за юліанським календарем, а в наступні роки за григоріанським календарем.

**`CAL_EASTER_ALWAYS_GREGORIAN`**(int)

Для[easter\_days()](function.easter-days.md): обчислювати Великдень відповідно до пролептичного григоріанського календаря

**`CAL_EASTER_ALWAYS_JULIAN`**(int)

Для[easter\_days()](function.easter-days.md): обчислювати Великдень відповідно до юліанського календаря

**`CAL_GREGORIAN`**(int)

Для[cal\_days\_in\_month()](function.cal-days-in-month.md) [cal\_from\_jd()](function.cal-from-jd.md) [cal\_info()](function.cal-info.md) і [cal\_to\_jd()](function.cal-to-jd.md): використовувати пролептичний григоріанський календар

**`CAL_JULIAN`**(int)

Для[cal\_days\_in\_month()](function.cal-days-in-month.md) [cal\_from\_jd()](function.cal-from-jd.md) [cal\_info()](function.cal-info.md) і [cal\_to\_jd()](function.cal-to-jd.md): використовувати юліанський календар

**`CAL_JEWISH`**(int)

Для[cal\_days\_in\_month()](function.cal-days-in-month.md) [cal\_from\_jd()](function.cal-from-jd.md) [cal\_info()](function.cal-info.md) і [cal\_to\_jd()](function.cal-to-jd.md): використовувати єврейський календар

**`CAL_FRENCH`**(int)

Для[cal\_days\_in\_month()](function.cal-days-in-month.md) [cal\_from\_jd()](function.cal-from-jd.md) [cal\_info()](function.cal-info.md) і [cal\_to\_jd()](function.cal-to-jd.md): використовувати французький республіканський календар.

**`CAL_NUM_CALS`**(int)

Кількість доступних календарів.

**`CAL_JEWISH_ADD_ALAFIM_GERESH`**(int)

Для[jdtojewish()](function.jdtojewish.md): додає знак горіш (geresh), що нагадує одинарну лапку як роздільник тисяч для кількості років.

**`CAL_JEWISH_ADD_ALAFIM`**(int)

Для[jdtojewish()](function.jdtojewish.md): додає слово alafim як роздільник тисяч для кількості років.

**`CAL_JEWISH_ADD_GERESHAYIM`**(int)

For[jdtojewish()](function.jdtojewish.md): додати символ гершаїм (gershayim), що нагадує подвійну лапку перед останньою літерою дня та числом років

**`CAL_DOW_DAYNO`**(int)

Для[jddayofweek()](function.jddayofweek.md): день тижня у вигляді цілого числа (int), де означає неділю, а `6`означает субботу.

**`CAL_DOW_SHORT`**(int)

Для[jddayofweek()](function.jddayofweek.md): скорочена англійська назва дня тижня

**`CAL_DOW_LONG`**(int)

Для[jddayofweek()](function.jddayofweek.md): англійська назва дня тижня.

**`CAL_MONTH_GREGORIAN_SHORT`**(int)

Для[jdmonthname()](function.jdmonthname.md): скорочена григоріанська назва місяця

**`CAL_MONTH_GREGORIAN_LONG`**(int)

Для[jdmonthname()](function.jdmonthname.md): григоріанська назва місяця

**`CAL_MONTH_JULIAN_SHORT`**(int)

Для[jdmonthname()](function.jdmonthname.md): скорочена юліанська назва місяця

**`CAL_MONTH_JULIAN_LONG`**(int)

Для[jdmonthname()](function.jdmonthname.md): юліанська назва місяця.

**`CAL_MONTH_JEWISH`**(int)

Для[jdmonthname()](function.jdmonthname.md): єврейська назва місяця.

**`CAL_MONTH_FRENCH`**(int)

Для[jdmonthname()](function.jdmonthname.md): французька республіканська назва місяця
