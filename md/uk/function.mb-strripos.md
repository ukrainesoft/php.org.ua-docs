- [«mb_strrichr](function.mb-strrichr.md)
- [mb_strrpos »](function.mb-strrpos.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Пошук останнього входження одного рядка в інший, нечутливий до
регістру

#mb_strripos

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

mb_strripos — Пошук останнього входження одного рядка до іншого,
нечутливий до регістру

### Опис

**mb_strripos**(
string `$haystack`,
string `$needle`,
int `$offset` = 0,
?string `$encoding` = **`null`**
): int\|false

**mb_strripos()** виконує безпечну з погляду багатобайтних
кодування операцію [strripos()](function.strripos.md), спираючись на
кількість символів. Позиція рядка `needle` розраховується з початку
рядки `haystack`. Позиція першого символу 0. Другого символу 1.
на відміну від [mb_strrpos()](function.mb-strrpos.md), **mb_strripos()**
не чутлива до регістру.

### Список параметрів

`haystack`
Рядок, в якому проводиться пошук входження `needle`

`needle`
Рядок, пошук якого проводиться в рядку `haystack`

`offset`
Позиція у рядку `haystack`, з якої починається пошук входжень

`encoding`
Кодування рядків символів. Якщо задана, буде використана внутрішня
кодування скрипта.

### Значення, що повертаються

Повертає позицію останнього входження рядка `needle` у рядку
`haystack` або **`false`**, якщо `needle` не знайдена.

### Список змін

| Версія | Опис                                                     |
|--------|----------------------------------------------------------|
| 8.0.0  | needle тепер приймає порожній рядок.                     |
| 8.0.0  | Тепер параметр encoding може набувати значення **null**. |

### Дивіться також

- [strripos()](function.strripos.md) - Повертає позицію останнього
входження підрядки без урахування регістру
- [strrpos()](function.strrpos.md) - Повертає позицію останнього
входження підрядки у рядку
- [mb_strrpos()](function.mb-strrpos.md) - Пошук позиції останнього
входження одного рядка в інший
