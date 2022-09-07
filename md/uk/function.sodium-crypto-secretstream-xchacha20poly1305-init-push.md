---
navigation:
  - function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.md: « sodiumcryptosecretstreamxchacha20poly1305initpull
  - function.sodium-crypto-secretstream-xchacha20poly1305-keygen.md: sodiumcryptosecretstreamxchacha20poly1305keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretstreamxchacha20poly1305initpush
---
# sodiumcryptosecretstreamxchacha20poly1305initpush

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretstreamxchacha20poly1305initpush - Ініціалізує контекст secretstream для шифрування

### Опис

```methodsynopsis
sodium_crypto_secretstream_xchacha20poly1305_init_push(string $key): array
```

Ініціалізує контекст secretstream для шифрування

### Список параметрів

`key`

Ключ криптографії. Дивіться [sodiumcryptosecretstreamxchacha20poly1305keygen()](function.sodium-crypto-secretstream-xchacha20poly1305-keygen.md)

### Значення, що повертаються

Масив із двома рядковими значеннями:

-   Стан secretstream, необхідний подальших дій
-   Заголовок secretstream, який необхідно надати одержувачу, щоб він міг витягувати дані.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptosecretstreamxchacha20poly1305initpush()****

```php
<?php
function encrypt_file(string $inputFilePath, string $outputFilePath, string $key): void
{
    [$state, $header] = sodium_crypto_secretstream_xchacha20poly1305_init_push($key);

    $inputFile = fopen($inputFilePath, 'rb');
    $outputFile = fopen($outputFilePath, 'wb');
    // Запись заголовка:
    fwrite($outputFile, $header);
    $inputFileSize = fstat($inputFile)['size'];

    // Зашифровка файла и запись его содержимого в выходной файл:
    for ($i = 0; $i < $inputFileSize; $i += 8175) {
        $ptxt_chunk = fread($inputFile, 8175);
        $ctxt_chunk = sodium_crypto_secretstream_xchacha20poly1305_push($state, $ptxt_chunk);
        fwrite($outputFile, $ctxt_chunk);
    }

    sodium_memzero($state);
    fclose($inputFile);
    fclose($outputFile);
}

// sodium_crypto_secretstream_xchacha20poly1305_keygen()
$key = sodium_base642bin('MS0lzb7HC+thY6jY01pkTE/cwsQxnRq0/2L1eL4Hxn8=', SODIUM_BASE64_VARIANT_ORIGINAL);

file_put_contents('hello.txt', 'Hello world!');
encrypt_file('hello.txt', 'hello.txt.encrypted', $key);
var_dump(sodium_bin2hex(file_get_contents('hello.txt.encrypted')));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(106) "971e33b255f0990ef3931caf761c59136efa77b434832f28ec719e3ff73f5aec38b3bba1574ab5b70a8844d8da36a668e802cfea2c"
```
