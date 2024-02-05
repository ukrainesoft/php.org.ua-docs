---
navigation:
  - function.sodium-crypto-stream-xchacha20-keygen.md: « sodium\_crypto\_stream\_xchacha20\_keygen
  - function.sodium-crypto-stream-xchacha20-xor.md: sodium\_crypto\_stream\_xchacha20\_xor »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream\_xchacha20\_xor\_ic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream\_xchacha20\_xor\_ic

(PHP 8 >= 8.2.0)

sodium\_crypto\_stream\_xchacha20\_xor\_ic — Шифрує повідомлення, використовуючи неясний код та секретний ключ (без автентифікації)

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20_xor_ic(    string $message,    string $nonce,    int $counter,    string $key): string
```

Функция аналогична[sodium\_crypto\_stream\_xchacha20\_xor()](function.sodium-crypto-stream-xchacha20-xor.md)але додає можливість встановити початкове значення лічильника блоків у ненульове значення. Це дозволяє отримати прямий доступ до будь-якого блоку без необхідності обчислення попередніх.

**Застереження**

Це шифрування є неавтентифікованим і не запобігає атакам з підібраним шифротексту. Обов'язково об'єднайте шифротекст із кодом автентифікації повідомлення, наприклад, за допомогою функції [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md) або [sodium\_crypto\_auth()](function.sodium-crypto-auth.md)

### Список параметрів

`message`

Повідомлення для шифрування.

`nonce`

24-байтовий одноразовий номер.

`counter`

Початкове значення лічильника блоків.

`key`

Ключ, можливо, згенерований функцією [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)

### Значення, що повертаються

Повертає зашифроване повідомлення або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_stream\_xchacha20\_xor\_ic()\*\*\*\*

```php
<?php
$n2 = random_bytes(SODIUM_CRYPTO_STREAM_XCHACHA20_NONCEBYTES);
$left  = str_repeat("\x01", 64);
$right = str_repeat("\xfe", 64);

// Всё сразу:
$stream7_unified = sodium_crypto_stream_xchacha20_xor($left . $right, $n2, $key);

// По частям, с начальным счётчиком:
$stream7_left  = sodium_crypto_stream_xchacha20_xor_ic($left, $n2, 0, $key);
$stream7_right = sodium_crypto_stream_xchacha20_xor_ic($right, $n2, 1, $key);
$stream7_concat = $stream7_left . $stream7_right;

var_dump(strlen($stream7_concat));
var_dump($stream7_unified === $stream7_concat);
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(128)
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_stream\_xchacha20\_xor()](function.sodium-crypto-stream-xchacha20-xor.md) \- Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без аутентифікації)
