---
navigation:
  - function.mailparse-rfc822-parse-addresses.md: « mailparse\_rfc822\_parse\_addresses
  - function.mailparse-uudecode-all.md: mailparse\_uudecode\_all »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_stream\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_stream\_encode

(PECL mailparse >= 0.9.0)

mailparse\_stream\_encode — кодує потік із файлу джерела та пише у файл одержувач.

### Опис

```methodsynopsis
mailparse_stream_encode(resource $sourcefp, resource $destfp, string $encoding): bool
```

Кодує за допомогою `encoding` потік з файлу джерела та пише у файл одержувач.

### Список параметрів

`sourcefp`

Коректний файловий дескриптор джерела.

`destfp`

Коректний файловий дескриптор одержувача.

`encoding`

Одне з кодувань, підтримуваних модулем [mbstring](ref.mbstring.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mailparse\_stream\_encode()\*\*\*\*

```php
<?php

// email.eml содержит: hello, this is some text=hello.
$fp = fopen('email.eml', 'r');

$dest = tmpfile();

mailparse_stream_encode($fp, $dest, "quoted-printable");

rewind($dest);

// Отображаем контент нового файла
fpassthru($dest);

?>
```

Результат виконання наведеного прикладу:

```
hello, this is some text=3Dhello.
```
