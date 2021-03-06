- [« Функції gettext](ref.gettext.md)
- [bindtextdomain »](function.bindtextdomain.md)

- [PHP Manual](index.md)
- [Функції gettext](ref.gettext.md)
- Встановлює або отримує кодування, в якому повертатимуться
повідомлення з каталогу повідомлень домену

# bind_textdomain_codeset

(PHP 4 \>= 4.2.0, PHP 5, PHP 7, PHP 8)

bind_textdomain_codeset — Встановлює або отримує кодування в
якій повертатимуться повідомлення з каталогу повідомлень домену

### Опис

**bind_textdomain_codeset**(string `$domain`, ?string `$codeset`):
string\|false

Функція **bind_textdomain_codeset()** встановлює чи отримує
кодування, в якому повертатимуться повідомлення з `domain`, такими
функціями як [gettext()](function.gettext.md).

### Список параметрів

`domain`
Домен.

`codeset`
Кодування. Якщо **`null`**, повертається поточна встановлена
кодування.

### Значення, що повертаються

Рядок у разі успішного виконання.

### Список змін

| Версія | Опис                                                                                                |
|--------|-----------------------------------------------------------------------------------------------------|
| 8.0.3  | codeset тепер допускає значення null. Раніше було неможливо отримати поточне встановлене кодування. |

### Примітки

> **Примітка**:
>
> Інформація **bind_textdomain_codeset()** зберігається для кожного
> процесу, а чи не для потоку.
