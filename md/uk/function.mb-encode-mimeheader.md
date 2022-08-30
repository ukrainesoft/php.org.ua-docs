Кодує рядок для MIME-заголовка

-   [« mbdetectorder](function.mb-detect-order.html)
    
-   [мбencodenumericentity »](function.mb-encode-numericentity.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
    
-   Кодує рядок для MIME-заголовка
    

# мбencodemimeheader

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбencodemimeheader — Кодує рядок для заголовка MIME

### Опис

```methodsynopsis
mb_encode_mimeheader(    string $string,    ?string $charset = null,    ?string $transfer_encoding = null,    string $newline = "\r\n",    int $indent = 0): string
```

Кодує рядок (`string`) (string) за схемою кодування MIME-заголовка.

### Список параметрів

`string`

Кодований рядок типу string. Її кодування має відповідати [мбinternalencoding()](function.mb-internal-encoding.html)

`charset`

`charset` задає ім'я кодування, в якому представлено рядок `string`. За замовчуванням значення визначається настройкою NLS (`mbstring.language`

`transfer_encoding`

`transfer_encoding` задає схему MIME-кодування. Це може бути або `"B"` (Base64), або `"Q"` (Quoted-Printable). За замовчуванням `"B"`

`newline`

`newline` задає мітку EOL (кінець рядка, end-of-line), за допомогою якої **мбencodemimeheader()** здійснює завершення рядків ("line-folding" - термін [» RFC](http://www.faqs.org/rfcs/rfc2822), що означає розділення рядків, довжина яких перевищує задане значення. Значення довжини зараз жорстко задано як 74 символи). За замовчуванням `"\r\n"` (CRLF).

`indent`

Відступ першого рядка (число символів у заголовку перед `string`

### Значення, що повертаються

Конвертований рядок (string), перетворений на ASCII.

### список змін

| Версия | Описание |
| --- | --- |
|  | `charset` і `transfer_encoding` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **мбencodemimeheader()****

```php
<?php
$name = "太郎"; // kanji
$mbox = "kru";
$doma = "gtinn.mon";
$addr = '"' . addcslashes(mb_encode_mimeheader($name, "UTF-7", "Q"), '"') . '" <' . $mbox . "@" . $doma . ">";
echo $addr;
?>
```

Результат виконання цього прикладу:

```
"=?UTF-7?Q?+WSqQzg-?=" <kru@gtinn.mon>
```

### Примітки

> **Зауваження**
> 
> Ця функція не розрахована виконання високорівневих розривів рядків (перенесення слів цілком і т.п.). Така поведінка може призвести до появи несподіваних прогалин у вихідному рядку.

### Дивіться також

-   [мбdecodemimeheader()](function.mb-decode-mimeheader.html) - Декодує рядок у MIME-заголовку