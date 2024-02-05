---
navigation:
  - function.openssl-public-encrypt.md: « openssl\_public\_encrypt
  - function.openssl-seal.md: openssl\_seal »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_random\_pseudo\_bytes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_random\_pseudo\_bytes

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

openssl\_random\_pseudo\_bytes - Генерує псевдовипадкову послідовність байт

### Опис

```methodsynopsis
openssl_random_pseudo_bytes(int $length, bool &$strong_result = null): string
```

Генерує рядок псевдовипадкових байт завдовжки `length`

Також, якщо встановити необов'язковий параметр `strong_result`, який передається за посиланням, то до нього запишеться **`true`**или**`false`**, Залежно від того, чи був використаний криптографічно сильний алгоритм.

### Список параметрів

`length`

Довжина рядка, що генерується. Має бути цілим позитивним числом, меншим або рівним `2147483647`. При використанні PHP спробує привести цей параметр до ненульового цілого числа.

`strong_result`

Якщо задано, то передану змінну буде записано **`true`**или**`false`**, Залежно від того, чи був використаний криптографічно сильний алгоритм.

### Значення, що повертаються

Повертає рядок випадкових байт.

### Помилки

Функция**openssl\_random\_pseudo\_bytes()** викидає виняток [Exception](class.exception.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `strong_result` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**openssl\_random\_pseudo\_bytes()\*\*\*\*

```php
<?php
for ($i = 1; $i <= 4; $i++) {
    $bytes = openssl_random_pseudo_bytes($i, $cstrong);
    $hex   = bin2hex($bytes);

    echo "Lengths: Bytes: $i and Hex: " . strlen($hex) . PHP_EOL;
    var_dump($hex);
    var_dump($cstrong);
    echo PHP_EOL;
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Lengths: Bytes: 1 and Hex: 2
string(2) "42"
bool(true)

Lengths: Bytes: 2 and Hex: 4
string(4) "dc6e"
bool(true)

Lengths: Bytes: 3 and Hex: 6
string(6) "288591"
bool(true)

Lengths: Bytes: 4 and Hex: 8
string(8) "ab86d144"
bool(true)
```

### Дивіться також

-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
-   [bin2hex()](function.bin2hex.md) \- Перетворює бінарні дані на шістнадцяткове подання
-   [crypt()](function.crypt.md) \- Необоротне хешування рядка
-   [random\_int()](function.random-int.md) \- Отримує криптографічно безпечне, рівномірно вибране ціле число
