---
navigation:
  - function.iconv-mime-decode.html: « iconvmimedecode
  - function.iconv-set-encoding.html: iconvsetencoding »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvmimeencode
---
# iconvmimeencode

(PHP 5, PHP 7, PHP 8)

iconvmimeencode — Створює поле `MIME`заголовка

### Опис

```methodsynopsis
iconv_mime_encode(string $field_name, string $field_value, array $options = []): string|false
```

Створює та повертає коректне поле `MIME`заголовка у вигляді рядка виду:

```
Subject: =?ISO-8859-1?Q?Pr=FCfung_f=FCr?= Entwerfen von einer MIME kopfzeile
```

У прикладі вище "Subject" є ім'ям поля, а частина рядка, починаючи з "=? ​​ISO-8859-1? ..." – Його значення.

### Список параметрів

`field_name`

Ім'я поля.

`field_value`

Значення поля.

`options`

Є можливість контролювати поведінку функції **iconvmimeencode()** за допомогою передачі масиву з налаштуваннями як третій аргумент `options`. Можливі значення цього масиву, що підтримуються функцією **iconvmimeencode()**, наведені нижче. Зверніть увагу, що імена елементів чутливі до регістру символів.

**Установки, що підтримуються в **iconvmimeencode()****

| Элемент | Тип | Описание | Значение по умолчанию | Пример |
| --- | --- | --- | --- | --- |
| scheme | string | Задає, як закодувати значення поля. Значенням цього елемента може бути "B", або "Q". "B" означає схему кодування `base64`, а "Q" - `quoted-printable` | У | У |
| input-charset | string | Задає, в якому кодуванні представлені аргументи `field_name` і `field_value`. Якщо не задано, **iconvmimeencode()** передбачає, що набір символів вказано в ini-налаштуванні [iconv.internalencoding](iconv.configuration.md) | [iconv.internalencoding](iconv.configuration.md) | ISO-8859-1 |
| output-charset | string | Задає набір символів, у якому буде представлений результат. `MIME`Заголовок. | [iconv.internalencoding](iconv.configuration.md) | UTF-8 |
| line-length | int | Встановлює максимальну довжину рядків заголовка. Якщо результуючий заголовок виявиться довшим за цю величину, функція його розріже на кілька рядків відповідно до [» Форматом інтернет повідомлень - RFC2822](http://www.faqs.org/rfcs/rfc2822). Якщо не встановлено, ця довжина буде встановлена ​​76 символами. |  |  |
| line-break-chars | string | Задає послідовність символів, які будуть використовуватися для завершення "розрізаних" рядків заголовка, якщо заголовок виявиться довшим за один рядок. Якщо не встановлено, будуть використовуватися символи "рn" (`CR` `LF`). Зверніть увагу, що цей аргумент завжди обробляється як рядок ASCII незалежно від значення `input-charset` | рн | н |

### Значення, що повертаються

Повертає закодоване `MIME`поле у ​​разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **iconvmimeencode()****

```php
<?php
$preferences = array(
    "input-charset" => "ISO-8859-1",
    "output-charset" => "UTF-8",
    "line-length" => 76,
    "line-break-chars" => "\n"
);
$preferences["scheme"] = "Q";
// Результат "Subject: =?UTF-8?Q?Pr=C3=BCfung=20Pr=C3=BCfung?="
echo iconv_mime_encode("Subject", "Prüfung Prüfung", $preferences);

$preferences["scheme"] = "B";
// Результат "Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?="
echo iconv_mime_encode("Subject", "Prüfung Prüfung", $preferences);
?>
```

### Дивіться також

-   [imapbinary()](function.imap-binary.md) - Конвертує 8-бітовий рядок у рядок base64
-   [мбencodemimeheader()](function.mb-encode-mimeheader.md) - Кодує рядок для MIME-заголовка
-   [imap8bit()](function.imap-8bit.md) - Конвертує 8-бітний рядок у рядок у форматі quoted-printable
-   [quotedprintableencode()](function.quoted-printable-encode.md) - Перетворює 8-бітовий рядок за допомогою методу quoted-printable
