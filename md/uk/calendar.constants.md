Обумовлені константи

-   [« Типы ресурсов](calendar.resources.html)
    
-   [Календарь »](ref.calendar.html)
    
-   [PHP Manual](index.html)
    
-   [Календарь](book.calendar.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`CAL_EASTER_DEFAULT`** (int)

Для [easterdays()](function.easter-days.html): обчислювати Великдень для років до 1753 за юліанським календарем, а в наступні роки за григоріанським календарем.

**`CAL_EASTER_ROMAN`** (int)

Для [easterdays()](function.easter-days.html): обчислювати Великдень для років до 1583 за юліанським календарем, а в наступні роки за григоріанським календарем.

**`CAL_EASTER_ALWAYS_GREGORIAN`** (int)

Для [easterdays()](function.easter-days.html): обчислювати Великдень відповідно до пролептичного григоріанського календаря

**`CAL_EASTER_ALWAYS_JULIAN`** (int)

Для [easterdays()](function.easter-days.html): обчислювати Великдень відповідно до юліанського календаря

**`CAL_GREGORIAN`** (int)

Для [caldaysінmonth()](function.cal-days-in-month.html) [calfromjd()](function.cal-from-jd.html) [calinfo()](function.cal-info.html) і [calтоjd()](function.cal-to-jd.html): використовувати пролептичний григоріанський календар

**`CAL_JULIAN`** (int)

Для [caldaysінmonth()](function.cal-days-in-month.html) [calfromjd()](function.cal-from-jd.html) [calinfo()](function.cal-info.html) і [calтоjd()](function.cal-to-jd.html): використовувати юліанський календар

**`CAL_JEWISH`** (int)

Для [caldaysінmonth()](function.cal-days-in-month.html) [calfromjd()](function.cal-from-jd.html) [calinfo()](function.cal-info.html) і [calтоjd()](function.cal-to-jd.html): використовувати єврейський календар

**`CAL_FRENCH`** (int)

Для [caldaysінmonth()](function.cal-days-in-month.html) [calfromjd()](function.cal-from-jd.html) [calinfo()](function.cal-info.html) і [calтоjd()](function.cal-to-jd.html): використовувати французький республіканський календар.

**`CAL_NUM_CALS`** (int)

Кількість календарів доступних.

**`CAL_JEWISH_ADD_ALAFIM_GERESH`** (int)

Для [jdtojewish()](function.jdtojewish.html): додає знак горіш (geresh), що нагадує одинарну лапку як роздільник тисяч для кількості років.

**`CAL_JEWISH_ADD_ALAFIM`** (int)

Для [jdtojewish()](function.jdtojewish.html): додає слово alafim як роздільник тисяч для кількості років.

**`CAL_JEWISH_ADD_GERESHAYIM`** (int)

For [jdtojewish()](function.jdtojewish.html): додати символ гершаїм (gershayim), що нагадує подвійну лапку перед останньою літерою дня та числом років

**`CAL_DOW_DAYNO`** (int)

Для [jddayofweek()](function.jddayofweek.html): день тижня у вигляді цілого числа (int), де `0` означає неділю, а `6` означає суботу.

**`CAL_DOW_SHORT`** (int)

Для [jddayofweek()](function.jddayofweek.html): скорочена англійська назва дня тижня

**`CAL_DOW_LONG`** (int)

Для [jddayofweek()](function.jddayofweek.html): англійська назва дня тижня.

**`CAL_MONTH_GREGORIAN_SHORT`** (int)

Для [jdmonthname()](function.jdmonthname.html): скорочена григоріанська назва місяця

**`CAL_MONTH_GREGORIAN_LONG`** (int)

Для [jdmonthname()](function.jdmonthname.html): григоріанська назва місяця

**`CAL_MONTH_JULIAN_SHORT`** (int)

Для [jdmonthname()](function.jdmonthname.html): скорочена юліанська назва місяця

**`CAL_MONTH_JULIAN_LONG`** (int)

Для [jdmonthname()](function.jdmonthname.html): юліанська назва місяця.

**`CAL_MONTH_JEWISH`** (int)

Для [jdmonthname()](function.jdmonthname.html): єврейська назва місяця.

**`CAL_MONTH_FRENCH`** (int)

Для [jdmonthname()](function.jdmonthname.html): французька республіканська назва місяця