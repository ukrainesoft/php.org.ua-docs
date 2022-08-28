Декодує поле MIME-заголовка

-   [« iconv\_mime\_decode\_headers](function.iconv-mime-decode-headers.html)
    
-   [iconv\_mime\_encode »](function.iconv-mime-encode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Декодує поле MIME-заголовка
    

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
|  | ICONVMIMEDECODECONTINUEВІНERROR | Якщо поставлено, [iconv\_mime\_decode\_headers()](function.iconv-mime-decode-headers.html) намагатиметься пропускати граматичні помилки та продовжувати обробку заголовка. |

`encoding`

Необов'язковий аргумент `encoding` задає набір символів, у якому буде представлено результат. Якщо аргумент опущено, використовуватиметься [iconv.internal\_encoding](iconv.configuration.html)

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

-   [iconv\_mime\_decode\_headers()](function.iconv-mime-decode-headers.html) - Декодує кілька полів заголовка MIME
-   [mb\_decode\_mimeheader()](function.mb-decode-mimeheader.html) - Декодує рядок у MIME-заголовку
-   [imap\_mime\_header\_decode()](function.imap-mime-header-decode.html) - Декодувати елементи заголовка
-   [imap\_base64()](function.imap-base64.html) - Декодувати текст закодований BASE64
-   [imap\_qprint()](function.imap-qprint.html) - Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок