- [« iconv_strrpos](function.iconv-strrpos.md)
- [iconv »](function.iconv.md)

- [PHP Manual](index.md)
- [Функції iconv](ref.iconv.md)
- Отримання частини рядка

# iconv_substr

(PHP 5, PHP 7, PHP 8)

iconv_substr — Отримання частини рядка

### Опис

**iconv_substr**(
string `$string`,
int `$offset`,
?int `$length` = **`null`**,
?string `$encoding` = **`null`**
): string\|false

Отримує частину рядка `string`, визначену параметрами `offset` та
`length`.

### Список параметрів

`string`
Початковий рядок.

`offset`
Якщо `offset` невід'ємний, **iconv_substr()** отримує частину рядка
`string` починаючи з символу з порядковим номером `offset` (нумерація
починається з нуля).

Якщо `offset` негативний, **iconv_substr()** отримує частину рядка
починаючи з позиції, що віддалена від кінця рядка `string` на `offset`
символів.

`length`
Якщо `length` заданий і позитивний, значення, що повертається містить не
більше `length` символів, починаючи з `offset` (залежить від довжини рядка
`string`).

Якщо вказано негативний `length`, **iconv_substr()** отримує частину
рядки `string`, починаючи з `offset` символу і до символу, віддаленого від
кінця рядка на 'length' символів. У випадку, якщо `offset` також
негативний, стартова позиція обчислюється заздалегідь відповідно до
вищеописаним правилом.

`encoding`
Якщо параметр `encoding` не вказано, передбачається, що рядок `string`
має кодування [iconv.internal_encoding](iconv.configuration.md).

Зверніть увагу, що і `offset`, і `length` ґрунтуються на розмірі
символу, розрахованого виходячи з кодування тексту (`encoding`),
час як подібна функція [substr()](function.substr.md) завжди
розглядає їх побайтове усунення.

### Значення, що повертаються

Повертає частину рядка `string`, визначену параметрами `offset` та
`length`.

Якщо рядок `string` має меншу довжину, ніж параметр `offset`, буде
повернено **`false`**. Якщо `string` має довжину рівну `offset`, буде
повернено порожній рядок.

### Список змін

| Версія | Опис                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------|
| 8.0.0  | length та encoding тепер допускають значення null.                                                                   |
| 7.0.11 | Якщо string має довжину рівну offset, буде повернуто порожній рядок. Раніше в подібних випадках поверталося 'false'. |

### Дивіться також

- [substr()](function.substr.md) - Повертає підрядок
- [mb_substr()](function.mb-substr.md) - Повертає частину рядка
- [mb_strcut()](function.mb-strcut.md) - Отримання частини рядка
