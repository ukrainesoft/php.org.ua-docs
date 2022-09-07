---
navigation:
  - function.openssl-public-encrypt.md: « opensslpublicencrypt
  - function.openssl-seal.md: opensslseal »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslrandompseudobytes
---
# opensslrandompseudobytes

(PHP 5> = 5.3.0, PHP 7, PHP 8)

opensslrandompseudobytes - Генерує псевдовипадкову послідовність байт

### Опис

```methodsynopsis
openssl_random_pseudo_bytes(int $length, bool &$strong_result = null): string
```

Генерує рядок псевдовипадкових байт завдовжки `length`

Також, якщо встановити необов'язковий параметр `strong_result`, Який передається за посиланням, то в нього запишеться **`true`** або **`false`**, Залежно від того, чи був використаний криптографічно сильний алгоритм.

### Список параметрів

`length`

Довжина рядка, що генерується. Має бути цілим позитивним числом, меншим або рівним `2147483647`. При використанні PHP спробує привести цей параметр до ненульового цілого числа.

`strong_result`

Якщо задано, то передану змінну буде записано **`true`** або **`false`**, Залежно від того, чи був використаний криптографічно сильний алгоритм.

### Значення, що повертаються

Повертає рядок випадкових байт.

### Помилки

Функція **opensslrandompseudobytes()** викидає виняток [Exception](class.exception.md) у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `strong_result` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **opensslrandompseudobytes()****

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

Результатом виконання цього прикладу буде щось подібне:

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

-   [randombytes()](function.random-bytes.md) - Генерує криптографічно безпечні псевдовипадкові байти
-   [bin2hex()](function.bin2hex.md) - Перетворює бінарні дані на шістнадцяткове подання
-   [crypt()](function.crypt.md) - Необоротне хешування рядка
-   [мтrand()](function.mt-rand.md) - Генерує випадкове значення методом за допомогою генератора простих чисел на базі Вихря Мерсенна
-   [uniqid()](function.uniqid.md) - Згенерувати унікальний ID
