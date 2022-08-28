Кодує потік з джерела файлу і пише у файл одержувач.

-   [« mailparse\_rfc822\_parse\_addresses](function.mailparse-rfc822-parse-addresses.html)
    
-   [mailparse\_uudecode\_all »](function.mailparse-uudecode-all.html)
    
-   [PHP Manual](index.html)
    
-   [Mailparse](ref.mailparse.html)
    
-   Кодує потік з джерела файлу і пише у файл одержувач.
    

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

Одне з кодувань, підтримуваних модулем [mbstring](ref.mbstring.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mailparsestreamencode()****

```php
<?php

// email.eml содержит: hello, this is some text=hello.
$fp = fopen('email.eml', 'r');

$dest = tmpfile();

mailparse_stream_encode($fp, $dest, "quoted-printable");

rewind($dest);

// Отображаем контент нового файла
fpassthru($dest);

?>
```

Результат виконання цього прикладу:

```
hello, this is some text=3Dhello.
```