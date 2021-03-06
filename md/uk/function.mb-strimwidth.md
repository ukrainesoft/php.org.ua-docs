- [«mb_strcut](function.mb-strcut.md)
- [mb_stripos »](function.mb-stripos.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Отримання рядка, обрізаного до заданого розміру

#mb_strimwidth

(PHP 4 \>= 4.0.6, PHP 5, PHP 7, PHP 8)

mb_strimwidth — Отримання рядка, обрізаного до заданого розміру

### Опис

**mb_strimwidth**(
string `$string`,
int `$start`,
int `$width`,
string `$trim_marker` = "",
?string `$encoding` = **`null`**
): string

Обрізає рядок (string) `string` до довжини `width` символів, де символи
половинної ширини вважаються як `1`, а символи повної ширини вважаються
як `2`. Дивіться
[»http://www.unicode.org/reports/tr11/](http://www.unicode.org/reports/tr11/)
для отримання детальної інформації про ширину символів у Східній Азії.

### Список параметрів

`string`
Вихідний рядок.

`start`
Зміщення з початку рядка. Кількість символів від початку рядка (перший
символ стоїть у позиції 0). Якщо вказано від'ємне число, то відлік
йтиме з кінця рядка.

`width`
Розмір частини, що вирізується в символах. Негативні значення відраховуються
з кінця.

`trim_marker`
Рядок, який замінить кінець обрізаного рядка.

`encoding`
Параметр 'encoding' є символьним кодуванням. Якщо він
опущений або дорівнює **`null`**, замість нього буде використано значення
внутрішнього кодування.

### Значення, що повертаються

Обрізаний рядок. Якщо заданий четвертий аргумент trim_marker, то його
значенням заміщаються останні символи рядка, так що сумарний
розмір був не більше `width`.

### Список змін

| Версія | Опис                                                     |
|--------|----------------------------------------------------------|
| 8.0.0  | Тепер параметр encoding може набувати значення **null**. |
| 7.1.0  | Додана підтримка негативних start та width.              |

### Приклади

**Приклад #1 Приклад використання **mb_strimwidth()****

`<?phpecho mb_strimwidth("Hello World", 0, 10, "...");// Виведе "Hello W..."?> `

### Дивіться також

- [mb_strwidth()](function.mb-strwidth.md) - Повертає ширину
рядки
- [mb_internal_encoding()](function.mb-internal-encoding.md) -
Встановлення/отримання внутрішнього кодування скрипту
