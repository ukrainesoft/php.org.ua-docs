---
navigation:
  - function.mb-detect-order.md: « mb\_detect\_order
  - function.mb-encode-numericentity.md: mb\_encode\_numericentity »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_encode\_mimeheader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_encode\_mimeheader

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_encode\_mimeheader — Кодує рядок для заголовка MIME

### Опис

```methodsynopsis
mb_encode_mimeheader(    string $string,    ?string $charset = null,    ?string $transfer_encoding = null,    string $newline = "\r\n",    int $indent = 0): string
```

Кодує за схемою кодування MIME-заголовка, передану в параметр `string`строку (string).

### Список параметрів

`string`

Кодований рядок (string). Її кодування має бути таким самим, яке повертає функція [mb\_internal\_encoding()](function.mb-internal-encoding.md)

`charset`

Параметр`charset` задає ім'я кодування, в якому представлено рядок `string`. За замовчуванням значення визначається настройкою NLS (`mbstring.language`

`transfer_encoding`

Параметр`transfer_encoding` задає схему MIME-кодування. Це може бути або `«B»`(Base64), либо`«Q»`(Quoted-Printable). По умолчанию`«B»`

`newline`

Параметр`newline` задає мітку EOL (кінець рядка, end-of-line), якою функція **mb\_encode\_mimeheader()** завершує рядки (line-folding - термін [» RFC](http://www.faqs.org/rfcs/rfc2822), Що означає розбиття рядка довше заданої довжини на кілька рядків. Значення довжини жорстко встановлено (74 символи). За замовчуванням `«\r\n»`(CRLF).

`indent`

Відступ першого рядка (число символів у заголовку перед параметром `string`

### Значення, що повертаються

Повертає перетворену версію рядка (string) у кодуванні ASCII.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметри `charset`и`transfer_encoding` тепер можуть набувати значення null. |

### Приклади

**Приклад #1 Приклад использования функции**mb\_encode\_mimeheader()\*\*\*\*

```php
<?php

$name = "太郎"; // kanji
$mbox = "kru";
$doma = "gtinn.mon";
$addr = '"' . addcslashes(mb_encode_mimeheader($name, "UTF-7", "Q"), '"') . '" <' . $mbox . "@" . $doma . ">";
echo $addr;
?>
```

Результат виконання наведеного прикладу:

```
"=?UTF-7?Q?+WSqQzg-?=" <kru@gtinn.mon>
```

### Примітки

> **Зауваження** :
> 
> Ця функція не розрахована виконання високорівневих контекстуальних розривів рядків (перенесення слів цілком тощо. п.). Така поведінка може засмічити вихідний рядок несподіваними пробілами.

### Дивіться також

-   [mb\_decode\_mimeheader()](function.mb-decode-mimeheader.md) \- Декодує рядок у MIME-заголовку
