- [«substr_replace](function.substr-replace.md)
- [Trim »](function.trim.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Повертає підрядок

# substr

(PHP 4, PHP 5, PHP 7, PHP 8)

substr — Повертає підрядок

### Опис

**substr**(string `$string`, int `$offset`, ?int `$length` =
**`null`**): string

Повертає рядок рядка `string`, що починається з `offset` символу по
рахунку та довжиною `length` символів.

### Список параметрів

`string`
Вхідний рядок.

`offset`
Якщо `offset` невід'ємний, повертається підрядок починається з позиції
`offset` від початку рядка, рахуючи від нуля. Наприклад, у рядку
'abcdef', в позиції 0 знаходиться символ 'a', в позиції 2 - символ
''c'', і т.д.

Якщо `offset` негативний, повертається підрядок починається з
позиції, що віддаляє на `offset` символів від кінця рядка `string`.

Якщо `string` менше `offset` символів, буде повернено порожній рядок.

**Приклад #1 Використання негативного параметра `offset`**

` <?php$rest = substr("abcdef", -1); // повертає "f"$rest = substr("abcdef", -2); // повертає "ef"$rest = substr("abcdef", -3, 1); // повертає "d"?> `

`length`
Якщо `length` позитивний, рядок, що повертається, буде не довшим
`length` символів, починаючи з параметра `offset` (залежно від довжини
`string`).

Якщо `length` негативний, то буде відкинуто зазначене цим
аргументом число символів з кінця рядка `string` (після того, як буде
обчислена стартова позиція, якщо `offset` негативний). Якщо при цьому
позиція початку підрядка, що визначається аргументом `offset`, знаходиться в
відкинутої частини рядка або за нею, повертається порожній рядок.

Якщо параметр `length` заданий і дорівнює `0`, буде повернено порожню
рядок.

Якщо параметр `length` опущений або **`null`**, то буде повернено
підрядок, що починається з позиції, вказаної параметром `offset` і
триває до кінця рядка.

**Приклад #2 Використання негативного параметра `length`**

`<?php$rest==substr("abcdef", 0, -1); // повертає "abcde"$rest = substr("abcdef", 2, -1); // повертає "cde"$rest = substr("abcdef", 4, -4); // повертає ""; до PHP 8.0.0 поверталося false$rest = substr("abcdef", -3, -1); // повертає "de"?> `

### Значення, що повертаються

Повертає витягнуту частину параметра `string` або порожній рядок.

### Список змін

| Версія | Опис                                                                                                                                                                                              |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Параметр length тепер допускає значення null. Якщо значення параметра length явно задано як **null**, функція повертає підрядок, що закінчується в кінці рядка; раніше повертався порожній рядок. |
| 8.0.0  | Функція повертає порожній рядок там, де раніше повертала ** false **.                                                                                                                             |

### Приклади

**Приклад #3 Базове використання **substr()****

`<?phpecho substr('abcdef', 1); // bcdefecho substr ("abcdef", 1, null); // bcdef; до PHP 8.0.0 повертався пустий рядокecho substr('abcdef', 1, 3); // bcdecho substr ( 'abcdef', 0, 4); //abcdechosubstr('abcdef',0,8); //abcdefechosubstr('abcdef', -1, 1); // f// Отримати доступ до окремого символу в рядку//можно також за допомогою допомогою квадратних дужок$string = 'abcdef';echo $string[0]; // aecho $string[3]; // decho $string[strlen($string)-1]; // f?> `

**Приклад #4 **substr()** та приведення типів**

`<?phpclass apple {    public function __toString() {        return "green"; }}echo "1) ".var_export(substr("pear", 0, 2), true).PHP_EOL;echo "2) ".var_export(substr(54321, 0, 2), true).PHP_EOL;ech 3) ".var_export(substr(new apple(), 0, 2), true).PHP_EOL;echo "4) ".var_export(substr(true, 0, 1), true).PHP_EOL;echo "5) .var_export(substr(false, 0, 1), true).PHP_EOL;echo "6) ".var_export(substr("", 0, 1), true).PHP_EOL;echo "7) ".var_export(sub 1.2e3, 0, 4), true).PHP_EOL;?> `

Результат виконання цього прикладу:

1) 'pe'
2) '54'
3) 'gr'
4) '1'
5) ''
6) ''
7) '1200'

**Приклад #5 Неприпустимий діапазон символів**

Якщо запитується неприпустимий діапазон символів, **substr()**
повертає порожній рядок, починаючи з PHP 8.0.0; раніше поверталося
**`false`**.

` <?phpvar_dump(substr('a', 2));?> `

Результат виконання цього прикладу в PHP 8:

string(0) ""

]

Результат виконання цього прикладу в PHP 7:

bool(false)

### Дивіться також

- [strrchr()](function.strrchr.md) - Знаходить останнє входження
символу в рядку
- [substr_replace()](function.substr-replace.md) - Замінює частину
рядки
- [preg_match()](function.preg-match.md) - Виконує перевірку на
відповідність регулярному виразу
- [trim()](function.trim.md) - Видаляє пробіли (або інші символи)
з початку та кінця рядка
- [mb_substr()](function.mb-substr.md) - Повертає частину рядка
- [wordwrap()](function.wordwrap.md) - Переносить рядок по
вказаній кількості символів
- [Посимвольний доступ та зміна строки](language.types.string.md#language.types.string.substr)
