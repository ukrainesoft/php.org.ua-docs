---
navigation:
  - function.sodium-crypto-secretbox.html: « sodiumcryptosecretbox
  - function.sodium-crypto-secretstream-xchacha20poly1305-init-push.html: sodiumcryptosecretstreamxchacha20poly1305initpush »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretstreamxchacha20poly1305initpull
---
# sodiumcryptosecretstreamxchacha20poly1305initpull

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretstreamxchacha20poly1305initpull - Ініціалізує контекст secretstream для дешифрування

### Опис

```methodsynopsis
sodium_crypto_secretstream_xchacha20poly1305_init_pull(string $header, string $key): string
```

Ініціалізує контекст secretstream для дешифрування

### Список параметрів

`header`

Заголовок secretstream. Має бути одне із значень, створених [sodiumcryptosecretstreamxchacha20poly1305initpush()](function.sodium-crypto-secretstream-xchacha20poly1305-init-push.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Стан secretstream.

### Приклади

**Приклад #1 Приклад використання **sodiumcryptosecretstreamxchacha20poly1305initpull()****

```php
<?php
function decrypt_file(string $inputFilePath, string $outputFilePath, string $key): void
{
    $inputFile = fopen($inputFilePath, 'rb');
    $outputFile = fopen($outputFilePath, 'wb');
    $header = fread($inputFile, 24);

    $state = sodium_crypto_secretstream_xchacha20poly1305_init_pull($header, $key);
    $inputFileSize = fstat($inputFile)['size'];

    // Расшифровка файла и запись содержимого в выходной файл:
    for ($i = 24; $i < $inputFileSize; $i += 8192) {
        $ctxt_chunk = fread($inputFile, 8192);

        // Мы не используем $tag, но в реальных протоколах вы можете использовать его для шифрования, например,
        // инициировать смену ключа или указать конец файла. Затем при расшифровке
        // вы можете подтвердить это поведение.
        [$ptxt_chunk, $tag] = sodium_crypto_secretstream_xchacha20poly1305_pull($state, $ctxt_chunk);
        fwrite($outputFile, $ptxt_chunk);
    }

    sodium_memzero($state);
    fclose($inputFile);
    fclose($outputFile);
}

// sodium_crypto_secretstream_xchacha20poly1305_keygen()
$key = sodium_base642bin('MS0lzb7HC+thY6jY01pkTE/cwsQxnRq0/2L1eL4Hxn8=', SODIUM_BASE64_VARIANT_ORIGINAL);

$example = sodium_hex2bin('971e33b255f0990ef3931caf761c59136efa77b434832f28ec719e3ff73f5aec38b3bba1574ab5b70a8844d8da36a668e802cfea2c');
file_put_contents('hello.enc', $example);
decrypt_file('hello.enc', 'hello.txt.decrypted', $key);
var_dump(file_get_contents('hello.txt.decrypted'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(12) "Hello world!"
```
