---
navigation:
  - function.imap-lsub.md: « imaplsub
  - function.imap-mail-copy.md: imapmailcopy »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapmailcompose
---
# imapmailcompose

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmailcompose — Створити MIME-повідомлення на основі заданих обгортки та тіла

### Опис

```methodsynopsis
imap_mail_compose(array $envelope, array $bodies): string|false
```

Створює MIME-повідомлення на основі обгортки `envelope` і тіла `bodies`

### Список параметрів

`envelope`

Асоціативний масив із полями заголовка. Допустимі ключі: `"remail"` `"return_path"` `"date"` `"from"` `"reply_to"` `"in_reply_to"` `"subject"` `"to"` `"cc"` `"bcc"` і `"message_id"`, які встановлюють відповідні заголовки повідомлень у заданий рядок (string). Для встановлення додаткових заголовків підтримується ключ `"custom_headers"`, який містить асоціативний масив інших заголовків, наприклад, `["User-Agent: My Mail Client"]`

`bodies`

Індексований масив тел. Перше тіло – це основна частина повідомлення; подальші тіла обробляються тільки якщо воно з типом **`TYPEMULTIPART`**; ці тіла становлять тіла частин.

**Структура масиву тіла**

| Ключ | Тип | Описание |
| --- | --- | --- |
| `type` | int | Тип MIME. Один з **`TYPETEXT`** (за замовчуванням), **`TYPEMULTIPART`** **`TYPEMESSAGE`** **`TYPEAPPLICATION`** **`TYPEAUDIO`** **`TYPEIMAGE`** **`TYPEMODEL`** або **`TYPEOTHER`** |
| `encoding` | int | Значення `Content-Transfer-Encoding`. Одне з **`ENC7BIT`** (default), **`ENC8BIT`** **`ENCBINARY`** **`ENCBASE64`** **`ENCQUOTEDPRINTABLE`** або **`ENCOTHER`** |
| `charset` | string | Параметр charset типу MIME. |
| `type.parameters` | array | Асоціативний масив (array) імен параметрів `Content-Type` та їх значень. |
| `subtype` | string | Підтип MIME, наприклад, `'jpeg'` для **`TYPEIMAGE`** |
| `id` | string | Значення `Content-ID` |
| `description` | string | Значення `Content-Description` |
| `disposition.type` | string | Значення `Content-Disposition`, наприклад, `'attachment'` |
| `disposition` | array | Асоціативний масив (array) імен параметрів `Content-Disposition` та їх значень. |
| `contents.data` | string | Корисне навантаження. |
| `lines` | int | Розмір корисного навантаження у рядках. |
| `bytes` | int | Розмір корисного навантаження у байтах. |
| `md5` | string | Контрольна сума MD5 корисного навантаження. |

### Значення, що повертаються

Повертає MIME-повідомлення у вигляді рядка (string) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **imapmailcompose()****

```php
<?php

$envelope["from"]= "joe@example.com";
$envelope["to"]  = "foo@example.com";
$envelope["cc"]  = "bar@example.com";

$part1["type"] = TYPEMULTIPART;
$part1["subtype"] = "mixed";

$filename = "/tmp/imap.c.gz";
$fp = fopen($filename, "r");
$contents = fread($fp, filesize($filename));
fclose($fp);

$part2["type"] = TYPEAPPLICATION;
$part2["encoding"] = ENCBINARY;
$part2["subtype"] = "octet-stream";
$part2["description"] = basename($filename);
$part2["contents.data"] = $contents;

$part3["type"] = TYPETEXT;
$part3["subtype"] = "plain";
$part3["description"] = "description3";
$part3["contents.data"] = "contents.data3\n\n\n\t";

$body[1] = $part1;
$body[2] = $part2;
$body[3] = $part3;

echo nl2br(imap_mail_compose($envelope, $body));

?>
```
