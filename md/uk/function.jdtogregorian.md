- [«jdtofrench](function.jdtofrench.md)
- [jdtojewish »](function.jdtojewish.md)

- [PHP Manual](index.md)
- [Календарь](ref.calendar.md)
- Переводить число днів у юліанському літочисленні в дату по
Григоріанському календарю

#jdtogregorian

(PHP 4, PHP 5, PHP 7, PHP 8)

jdtogregorian — Переказує число днів у юліанському літочисленні в дату
за Григоріанським календарем

### Опис

**jdtogregorian**(int `$julian_day`): string

Переводить число днів у юліанському літочисленні в рядок, що містить
григоріанську дату у форматі "місяць/день/рік".

### Список параметрів

`julian_day`
Номер дня у юліанському літочисленні у вигляді цілого числа

### Значення, що повертаються

Дата за григоріанським календарем у вигляді рядка формату "місяць/день/рік"

### Дивіться також

- [gregoriantojd()](function.gregoriantojd.md) - Перетворює дату за
григоріанському календарю в кількість днів у юліанському
літочисленні
- [cal_from_jd()](function.cal-from-jd.md) - Перетворює дату,
задану в юліанському календарі, в дату вказаного календаря
