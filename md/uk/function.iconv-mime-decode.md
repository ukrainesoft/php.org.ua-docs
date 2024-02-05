---
navigation:
  - function.iconv-mime-decode-headers.md: « iconv\_mime\_decode\_headers
  - function.iconv-mime-encode.md: iconv\_mime\_encode »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_mime\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_mime\_decode

(PHP 5, PHP 7, PHP 8)

iconv\_mime\_decode — Декодирует поле`MIME`\-заголовка

### Опис

```methodsynopsis
iconv_mime_decode(string $string, int $mode = 0, ?string $encoding = null): string|false
```

Декодирует поле`MIME`\-заголовка.

### Список параметрів

`string`

Закодований заголовок у вигляді рядка.

`mode`

`mode` задає режим поведінки функції у разі, коли **iconv\_mime\_decode()** визначить, що `MIME`\-заголовок має неприпустиму структуру. Режим задається комбінацією наступних бітових масок.

**Бітові маски, що застосовуються в **iconv\_mime\_decode()****

| Значение | Константа | Опис |
| --- | --- | --- |
|  | ICONV\_MIME\_DECODE\_STRICT | Якщо встановлено, заголовок декодується в повній відповідності до стандарту [» RFC2047](http://www.faqs.org/rfcs/rfc2047). . Ця опція відключена за замовчуванням, оскільки існує безліч поштових програм, які не дотримуються специфікацій та формують некоректні з погляду стандарту `MIME`\-заголовки. |
|  | ICONV\_MIME\_DECODE\_CONTINUE\_ON\_ERROR | Якщо поставлено, [iconv\_mime\_decode\_headers()](function.iconv-mime-decode-headers.md) намагатиметься пропускати граматичні помилки та продовжувати обробку заголовка. |

`encoding`

Необов'язковий аргумент `encoding` задає набір символів, у якому буде представлено результат. Якщо аргумент опущено, використовуватиметься [iconv.internal\_encoding](iconv.configuration.md)

### Значення, що повертаються

Повертає декодований `MIME`\-заголовок у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `encoding` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** iconv\_mime\_decode()\*\*\*\*

```php
<?php
// Выдаст в результате "Subject: Prüfung Prüfung"
echo iconv_mime_decode("Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?=",
                       0, "ISO-8859-1");
?>
```

### Дивіться також

-   [iconv\_mime\_decode\_headers()](function.iconv-mime-decode-headers.md) \- Декодує кілька полів заголовка MIME
-   [mb\_decode\_mimeheader()](function.mb-decode-mimeheader.md) \- Декодує рядок у MIME-заголовку
-   [imap\_mime\_header\_decode()](function.imap-mime-header-decode.md) \- декодує елементи заголовка
-   [imap\_base64()](function.imap-base64.md) \- Декодує закодований BASE64 текст
-   [imap\_qprint()](function.imap-qprint.md) \- Перетворює рядок з формату quoted-printable на 8-бітовий рядок
