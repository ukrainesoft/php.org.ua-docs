---
navigation:
  - function.mcrypt-enc-self-test.html: « mcryptencselftest
  - function.mcrypt-generic-deinit.html: mcryptgenericdeinit »
  - index.html: PHP Manual
  - ref.mcrypt.html: Mcrypt
title: mcryptencrypt
---
# mcryptencrypt

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencrypt — Шифрує текст із заданими параметрами

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_encrypt(    string $cipher,    string $key,    string $data,    string $mode,    string $iv = ?): string|false
```

Шифрує дані.

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`key`

Ключ, з яким шифруватимуться дані. Якщо довжина ключа не відповідає вимогам шифру, то буде повернуто **`false`** та видано попередження.

`data`

Дані, які будуть зашифровані за допомогою шифру `cipher` та режиму `mode`. Якщо розмір даних не кратний розміру блоку, вони будуть доповнені символами '`\0`

Розмір тексту, що повертається, може бути більше розміру вихідних даних `data`

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

`iv`

Використовується для ініціалізації в режимах CBC, CFB, OFB, а також деяких алгоритмах в режимі STREAM. Якщо переданий IV розмір не підтримується режимом зчеплення або IV не був переданий, а режим зчеплення його вимагає, функція згенерує попередження про помилку та поверне **`false`**

### Значення, що повертаються

Повертає рядок із зашифрованими даними або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mcryptencrypt()****

```php
<?php
    # --- ШИФРОВАНИЕ ---

    # ключ должен представлять собой случайную бинарную строку.
    # Для преобразовангия строки в ключ используйте scrypt, bcrypt или PBKDF2
    # Ключ задаётся в виде строки шестнадцатеричных чисел
    $key = pack('H*', "bcb04b7e103a0cd8b54763051cef08bc55abe029fdebae5e1d417e2ffb2a00a3");

    # Показываем длину ключа.
    # Длина ключа должна быть 16, 24 или 32 байт для AES-128, 192 и 256 соответственно
    $key_size =  strlen($key);
    echo "Длина ключа: " . $key_size . "\n";

    $plaintext = "This string was AES-256 / CBC / ZeroBytePadding encrypted.";

    # Создаём случайный инициализирующий вектор используя режим CBC
    $iv_size = mcrypt_get_iv_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
    $iv = mcrypt_create_iv($iv_size, MCRYPT_RAND);

    # Создаём шифрованный текст совместимыс с AES (размер блока = 128)
    # Подходит только для строк не заканчивающихся на 00h
    # (потому как это символ дополнения по умолчанию)
    $ciphertext = mcrypt_encrypt(MCRYPT_RIJNDAEL_128, $key,
                                 $plaintext, MCRYPT_MODE_CBC, $iv);

    # Добавляем инициализирующий вектор в начало, чтобы он был доступен для расшифровки
    $ciphertext = $iv . $ciphertext;

    # перекодируем зашифрованный текст в base64
    $ciphertext_base64 = base64_encode($ciphertext);

    echo  $ciphertext_base64 . "\n";

    # === ВНИМАНИЕ ===

    # Результирующий шифрованный текст не имеет целостности или аутентичности и не
    # защищён от атак padding oracle.

    # --- ДЕШИФРОВКА ---

    $ciphertext_dec = base64_decode($ciphertext_base64);

    # Извлекаем инициализирующий вектор. Длина вектора ($iv_size) должна совпадать
    # с тем, что возвращает функция mcrypt_get_iv_size()
    $iv_dec = substr($ciphertext_dec, 0, $iv_size);

    # Извлекаем зашифрованный текст
    $ciphertext_dec = substr($ciphertext_dec, $iv_size);

    # Отбрасываем завершающие символы 00h
    $plaintext_dec = mcrypt_decrypt(MCRYPT_RIJNDAEL_128, $key,
                                    $ciphertext_dec, MCRYPT_MODE_CBC, $iv_dec);

    echo  $plaintext_dec . "\n";
?>
```

Результат виконання цього прикладу:

```
Длина ключа: 32
ENJW8mS2KaJoNB5E5CoSAAu0xARgsR1bdzFWpEn+poYw45q+73az5kYi4j+0haevext1dGrcW8Qi59txfCBV8BBj3bzRP3dFCp3CPQSJ8eU=
This string was AES-256 / CBC / ZeroBytePadding encrypted.
```

### Дивіться також

-   [mcryptdecrypt()](function.mcrypt-decrypt.html) - Розшифровує дані із заданими параметрами
-   [mcryptmoduleopen()](function.mcrypt-module-open.html) - Відкриває модуль шифрування з використанням вказаних алгоритму та режиму
