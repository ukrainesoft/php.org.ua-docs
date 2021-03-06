- [«ps_get_parameter](function.ps-get-parameter.md)
- [ps_hyphenate »](function.ps-hyphenate.md)

- [PHP Manual](index.md)
- [Функції PS](ref.ps.md)
- Отримує певні значення

#ps_get_value

(PECL ps \>= 1.1.0)

ps_get_value — Отримує певні значення

### Опис

**ps_get_value**(resource `$psdoc`, string `$name`, float `$modifier` =
?): float

Отримує кілька значень, встановлених
[ps_set_value()](function.ps-set-value.md). Значення визначення
є значеннями з плаваючою точкою.

Параметр `name` може мати такі значення:

`fontsize`
Розмір поточного активного шрифту або шрифту, ідентифікатор якого
передається у параметрі `modifier`.

`font`
Поточний активний шрифт.

`imagewidth`
Ширина зображення, ідентифікатор якого передається у параметрі
`modifier`.

`imageheight`
Висота зображення, ідентифікатор якого передається у параметрі
`modifier`.

`capheight`
Висота великої літери M активного шрифту або шрифту, ідентифікатор
якого передається у параметрі `modifier`.

`ascender`
Верхній елемент активного шрифту або шрифту, ідентифікатор якого
передається у параметрі `modifier`.

`descender`
Нижчий елемент активного шрифту або шрифту, ідентифікатор якого
передається у параметрі `modifier`.

`italicangle`
Курсив активного шрифту або шрифту, ідентифікатор якого передається в
параметрі `modifier`.

`underlineposition`
Підкреслення активного шрифту або шрифту, ідентифікатор якого
передається у параметрі `modifier`.

`underlinethickness`
Товщина підкреслення активного шрифту або шрифту, ідентифікатор
якого передається у параметрі `modifier`.

`textx`
Поточна позиція на осі X для виведення тексту.

`texty`
Поточна позиція з осі Y для виведення тексту.

`textrendering`
Поточний режим відображення тексту.

`textrise`
Простір, на який текст піднімається над базовою лінією.

`leading`
Відстань між рядками тексту у точках.

`wordspacing`
Відстань між словами, кратна ширині символу пробілу.

`charspacing`
Пробіл між символами. Якщо charspacing не дорівнює 0.0, лігатури завжди
розчинятимуться.

`hyphenminchars`
Мінімальна кількість символів наприкінці слова.

`parindent`
Відступ першого n рядка абзацу.

`numindentlines`
Номер рядка в абзаці для відступу, якщо parindent не дорівнює 0,0.

`parskip`
Відстань між абзацами.

`linenumberspace`
Загальний простір перед кожним рядком для рядка.

`linenumbersep`
Пробіл між рядком та номером рядка.

`major`
Мажорна версія pslib.

`minor`
Мінорна версія pslib.

`subminor`, `revision`
Патч версія pslib.

### Список параметрів

`psdoc`
Ідентифікатор ресурсу файлу postscript, повернутий функцією
[ps_new()](function.ps-new.md).

`name`
Назва значення.

`modifier`
Параметр `modifier` вказує ресурс, для якого має бути отримано
значення. Це може бути ідентифікатор шрифту чи зображення.

### Значення, що повертаються

Повертає значення параметра або **false**.

### Дивіться також

- [ps_set_value()](function.ps-set-value.md) - Встановлює
певні значення
