---
navigation:
  - function.iconv-get-encoding.md: « iconvgetencoding
  - function.iconv-mime-decode.md: iconvmimedecode »
  - index.md: PHP Manual
  - ref.iconv.md: Функции iconv
title: iconvmimedecodeheaders
---
# iconvmimedecodeheaders

(PHP 5, PHP 7, PHP 8)

iconvmimedecodeheaders — Декодує кілька полів заголовка `MIME`

### Опис

```methodsynopsis
iconv_mime_decode_headers(string $headers, int $mode = 0, ?string $encoding = null): array|false
```

Декодує кілька полів заголовка `MIME` за один раз.

### Список параметрів

`headers`

Закодовані заголовки у вигляді рядка.

`mode`

Параметр `mode` визначає поведінку, якщо **iconvmimedecodeheaders()** виявить неправильне поле заголовка `MIME`. Можна вказати будь-яку комбінацію наступних бітових масок.

**Бітові маски **iconvmimedecodeheaders()****

| Значение | Константа | Описание |
| --- | --- | --- |
|  | ICONVMIMEDECODESTRICT | Строго дотримуватися стандартів, визначених у [» RFC2047](http://www.faqs.org/rfcs/rfc2047). За замовчуванням ця опція відключена, оскільки багато пропрієтарних програм електронної пошти не дотримуються стандартів і створюють некоректні заголовки `MIME` |
|  | ICONVMIMEDECODECONTINUEВІНERROR | Якщо встановлено, **iconvmimedecodeheaders()** намагатиметься ігнорувати будь-які помилки і продовжувати обробку поточного заголовка. |

`encoding`

Необов'язковий параметр `encoding` вказує кодування, в якому буде представлено результат. Якщо опущено, буде використано значення директиви [iconv.internalencoding](iconv.configuration.md)

### Значення, що повертаються

У разі успішного виконання повертає асоціативний масив із полями `MIME`заголовків, вказаних параметром `headers`, або **`false`** у разі виникнення помилки.

Кожен ключ елемента повертається масиву є окреме ім'я поля, а сам елемент - його значення. Якщо в заголовку є кілька полів з однаковим ім'ям, **iconvmimedecodeheaders()** автоматично поміщає їх у підмасив із числовими індексами в порядку їх обробки. Зверніть увагу, що імена заголовків не *нечутливі до регістру*

### список змін

| Версия | Описание |
| --- | --- |
|  | `encoding` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **iconvmimedecodeheaders()****

```php
<?php
$headers_string = <<<EOF
Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?=
To: example@example.com
Date: Thu, 1 Jan 1970 00:00:00 +0000
Message-Id: <example@example.com>
Received: from localhost (localhost [127.0.0.1]) by localhost
    with SMTP id example for <example@example.com>;
    Thu, 1 Jan 1970 00:00:00 +0000 (UTC)
    (envelope-from example-return-0000-example=example.com@example.com)
Received: (qmail 0 invoked by uid 65534); 1 Thu 2003 00:00:00 +0000

EOF;

$headers =  iconv_mime_decode_headers($headers_string, 0, "ISO-8859-1");
print_r($headers);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [Subject] => Prüfung Prüfung
    [To] => example@example.com
    [Date] => Thu, 1 Jan 1970 00:00:00 +0000
    [Message-Id] => <example@example.com>
    [Received] => Array
        (
            [0] => from localhost (localhost [127.0.0.1]) by localhost with SMTP id example for <example@example.com>; Thu, 1 Jan 1970 00:00:00 +0000 (UTC) (envelope-from example-return-0000-example=example.com@example.com)
            [1] => (qmail 0 invoked by uid 65534); 1 Thu 2003 00:00:00 +0000
        )

)
```

### Дивіться також

-   [iconvmimedecode()](function.iconv-mime-decode.md) - Декодує поле MIME-заголовка
-   [мбdecodemimeheader()](function.mb-decode-mimeheader.md) - Декодує рядок у MIME-заголовку
-   [imapmimeheaderdecode()](function.imap-mime-header-decode.md) - Декодувати елементи заголовка
-   [imapbase64()](function.imap-base64.md) - Декодувати текст закодований BASE64
-   [imapqprint()](function.imap-qprint.md) - Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок
