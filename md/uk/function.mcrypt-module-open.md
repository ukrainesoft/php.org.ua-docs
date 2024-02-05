---
navigation:
  - function.mcrypt-module-is-block-mode.md: « mcrypt\_module\_is\_block\_mode
  - function.mcrypt-module-self-test.md: mcrypt\_module\_self\_test »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_open

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_open — Відкриває модуль шифрування за допомогою вказаних алгоритмів і режимів.

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_open(    string $algorithm,    string $algorithm_directory,    string $mode,    string $mode_directory): resource
```

Відкриває модуль шифрування з використанням вказаних алгоритмів та режимів. Ім'я алгоритму задається його ім'ям, наприклад `"twofish"`, або за допомогою константи **`MCRYPT_ciphername`**. Закрити модуль можна за допомогою функції [mcrypt\_module\_close()](function.mcrypt-module-close.md)

### Список параметрів

`algorithm`

Одна из констант\*\*`MCRYPT_ciphername`\*\*или название алгоритма в виде строки.

`algorithm_directory`

Параметр`algorithm_directory` використовується для завдання місцезнаходження модуля шифрування. Якщо передати порожній рядок, то (`""`), то буде використано значення директиви `mcrypt.algorithms_dir` із php.ini. Якщо ж воно теж не задано, то буде використано стандартну директорію з якою компілювався libmcrypt (зазвичай /usr/local/lib/libmcrypt).

`mode`

Одна из констант\*\*`MCRYPT_MODE_modename`\*\*, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

`mode_directory`

Параметр`mode_directory` використовується для завдання місцезнаходження модуля режиму. Якщо передати порожній рядок, то (`""`), то буде використано значення директиви `mcrypt.modes_dir` із php.ini. Якщо ж воно теж не задано, то буде використано стандартну директорію, з якою компілювався libmcrypt (зазвичай /usr/local/lib/libmcrypt).

### Значення, що повертаються

Зазвичай повертається дескриптор шифрування або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mcrypt\_module\_open()\*\*\*\*

```php
<?php
    $td = mcrypt_module_open(MCRYPT_DES, '',
        MCRYPT_MODE_ECB, '/usr/lib/mcrypt-modes');

    $td = mcrypt_module_open('rijndael-256', '', 'ofb', '');
?>
```

У першому рядку прикладу ми намагаємося відкрити шифр `DES` з директорії за замовчуванням та використовувати режим `ECB` із директорії /usr/lib/mcrypt-modes. У другому прикладі використовуємо рядкові імена шифру та режиму, що працює лише з модулем, зібраним із бібліотекою libmcrypt 2.4.x or 2.5.x.

**Приклад #2 Приклад використання** mcrypt\_module\_open()\*\*\*\*

```php
<?php
    /* Открываем модуль шифрования */
    $td = mcrypt_module_open('rijndael-256', '', 'ofb', '');

    /* Создаём инициализирующий вектор и определяем длину ключа.
     * Для Windows используем MCRYPT_RAND */
    $iv = mcrypt_create_iv(mcrypt_enc_get_iv_size($td), MCRYPT_DEV_RANDOM);
    $ks = mcrypt_enc_get_key_size($td);

    /* Создаём ключ */
    $key = substr(md5('very secret key'), 0, $ks);

    /* Инициализируем шифрование */
    mcrypt_generic_init($td, $key, $iv);

    /* Шифруем данные */
    $encrypted = mcrypt_generic($td, 'This is very important data');

    /* Деинициализируем обработчик шифрования */
    mcrypt_generic_deinit($td);

    /* Инициализируем модуль дешифровки */
    mcrypt_generic_init($td, $key, $iv);

    /* Дешифруем данные */
    $decrypted = mdecrypt_generic($td, $encrypted);

    /* Деинициализируем обработчик дешифровки и закрываем модуль */
    mcrypt_generic_deinit($td);
    mcrypt_module_close($td);

    /* Печатаем строку */
    echo trim($decrypted) . "\n";
?>
```

### Дивіться також

-   [mcrypt\_module\_close()](function.mcrypt-module-close.md) \- Закриває модуль mcrypt
-   [mcrypt\_generic()](function.mcrypt-generic.md) \- Функція шифрує дані
-   [mdecrypt\_generic()](function.mdecrypt-generic.md) \- Дешифрування даних
-   [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) \- Функція ініціалізує всі буфери, необхідні для шифрування
-   [mcrypt\_generic\_deinit()](function.mcrypt-generic-deinit.md) \- Ця функція деініціалізує модуль шифрування
