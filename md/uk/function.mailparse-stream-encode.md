---
navigation:
  - function.mailparse-rfc822-parse-addresses.md: « mailparserfc822parseaddresses
  - function.mailparse-uudecode-all.md: mailparseuudecodeall »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsestreamencode
---
# mailparsestreamencode

(PECL mailparse >= 0.9.0)

mailparsestreamencode — кодує потік із файлу джерела та пише у файл одержувач.

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mailparsestreamencode()****

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

Результат виконання цього прикладу:

```
hello, this is some text=3Dhello.
```
