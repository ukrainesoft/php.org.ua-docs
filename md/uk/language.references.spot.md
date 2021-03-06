- [« Скидання змінних-посилань](language.references.unset.md)
- [Предвизначені змінні »](reserved.variables.md)

- [PHP Manual](index.md)
- [Пояснення посилань](language.references.md)
- Неявне використання механізму посилань

## Неявне використання механізму посилань

Багато синтаксичних конструкцій PHP реалізовані через механізм посилань,
тому все сказане вище про зв'язування застосовується також і до
цим конструкціям. Деякі конструкції, на кшталт передавальних та
повертають за посиланням, розглянуті раніше. Інші конструкції,
які використовують посилання:

### Посилання global

Якщо ви оголошуєте змінну як **global $var**, ви фактично
створюєте посилання на глобальну змінну. Це означає те саме, що
та:

` <?php$var =& $GLOBALS["var"];?> `

Це означає, наприклад, що скидання (unset) `$var` не призведе до скидання
глобальної змінної.
