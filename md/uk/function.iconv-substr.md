Отримання частини рядка

-   [« iconv\_strrpos](function.iconv-strrpos.html)
    
-   [iconv »](function.iconv.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Отримання частини рядка
    

# iconvsubstr

(PHP 5, PHP 7, PHP 8)

iconvsubstr — Отримання частини рядка

### Опис

```methodsynopsis
iconv_substr(    string $string,    int $offset,    ?int $length = null,    ?string $encoding = null): string|false
```

Отримує частину рядка `string`, визначену параметрами `offset` і `length`

### Список параметрів

`string`

Початковий рядок.

`offset`

Якщо `offset` негативний, **iconvsubstr()** отримує частину рядка `string` починаючи із символу з порядковим номером `offset` (Нумерація починається з нуля).

Якщо `offset` негативний, **iconvsubstr()** отримує частину рядка починаючи з позиції, що віддаляється від кінця рядка `string` на `offset` символів.

`length`

Якщо `length` заданий і позитивний, значення, що повертається містить не більше `length` символів, починаючи з `offset` (залежить від довжини рядка `string`

Якщо вказано негативний `length` **iconvsubstr()** отримує частину рядка `string`, починаючи з `offset` символу і до символу, віддаленого від кінця рядка на `length` символів. У разі якщо `offset` також негативний, стартова позиція обчислюється заздалегідь відповідно до вищеописаного правила.

`encoding`

Якщо параметр `encoding` не вказано, передбачається, що рядок `string` має кодування [iconv.internal\_encoding](iconv.configuration.html)

Зверніть увагу, що і `offset`, і `length` ґрунтуються на розмірі символу, розрахованого виходячи з кодування тексту (`encoding`), у той час як схожа функція [substr()](function.substr.html) завжди розглядає їх побайтове усунення.

### Значення, що повертаються

Повертає частину рядка `string`, визначену параметрами `offset` і `length`

Якщо рядок `string` має меншу довжину, ніж параметр `offset`, буде повернуто **`false`**. Якщо `string` має довжину рівну `offset`, буде повернуто порожній рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` і `encoding` тепер допускають значення null. |
|  | Якщо `string` має довжину рівну `offset`, буде повернуто порожній рядок. Раніше у таких випадках поверталося **`false`** |

### Дивіться також

-   [substr()](function.substr.html) - Повертає підрядок
-   [mb\_substr()](function.mb-substr.html) - Повертає частину рядка
-   [mb\_strcut()](function.mb-strcut.html) - Отримання частини рядка