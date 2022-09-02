---
navigation:
  - function.iconv-mime-decode-headers.md: « iconvmimedecodeheaders
  - function.iconv-mime-encode.md: iconvmimeencode »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvmimedecode
---
# iconvmimedecode

(PHP 5, PHP 7, PHP 8)

iconvmimedecode — Декодує поле `MIME`заголовка

### Опис

```methodsynopsis
iconv_mime_decode(string $string, int $mode = 0, ?string $encoding = null): string|false
```

Декодує поле `MIME`заголовка.

### Список параметрів

`string`

Закодований заголовок у вигляді рядка.

`mode`

`mode` задає режим поведінки функції у разі, коли **iconvmimedecode()** визначить, що `MIME`заголовок має неприпустиму структуру. Режим задається комбінацією наступних бітових масок.

**Бітові маски, що застосовуються в **iconvmimedecode()****

| Значение | Константа | Описание |
| --- | --- | --- |
|  | ICONVMIMEDECODESTRICT | Якщо задано, заголовок декодується у повній відповідності до стандарту [» RFC2047](http://www.faqs.org/rfcs/rfc2047). Ця опція відключена за замовчуванням, оскільки існує безліч поштових програм, які не дотримуються специфікацій та формують некоректні з погляду стандарту `MIME`заголовки. |
|  | ICONVMIMEDECODECONTINUEВІНERROR | Якщо поставлено, [iconvmimedecodeheaders()](function.iconv-mime-decode-headers.md) намагатиметься пропускати граматичні помилки та продовжувати обробку заголовка. |

`encoding`

Необов'язковий аргумент `encoding` задає набір символів, у якому буде представлено результат. Якщо аргумент опущено, використовуватиметься [iconv.internalencoding](iconv.configuration.md)

### Значення, що повертаються

Повертає декодований `MIME`заголовок у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `encoding` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **iconvmimedecode()****

```php
<?php
// Выдаст в результате "Subject: Prüfung Prüfung"
echo iconv_mime_decode("Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?=",
                       0, "ISO-8859-1");
?>
```

### Дивіться також

-   [iconvmimedecodeheaders()](function.iconv-mime-decode-headers.md) - Декодує кілька полів заголовка MIME
-   [мбdecodemimeheader()](function.mb-decode-mimeheader.md) - Декодує рядок у MIME-заголовку
-   [imapmimeheaderdecode()](function.imap-mime-header-decode.md) - Декодувати елементи заголовка
-   [imapbase64()](function.imap-base64.md) - Декодувати текст закодований BASE64
-   [imapqprint()](function.imap-qprint.md) - Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок
