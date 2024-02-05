---
navigation:
  - function.mcrypt-module-self-test.md: « mcrypt\_module\_self\_test
  - book.mhash.md: Mhash »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mdecrypt\_generic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mdecrypt\_generic

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mdecrypt\_generic - Дешифрування даних

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mdecrypt_generic(resource $td, string $data): string
```

Функція дешифрує дані. Зверніть увагу, що довжина рядка, що повертається, за фактом може бути більше довжини оригінального нешифрованого рядка. Це походить від того, що дані можуть доповнюватися.

### Список параметрів

`td`

Дескриптор шифрування, що повертається [mcrypt\_module\_open()](function.mcrypt-module-open.md)

`data`

Зашифровані дані.

### Значення, що повертаються

Повертає розшифрований рядок.

### Приклади

**Приклад #1 Приклад використання** mdecrypt\_generic()\*\*\*\*

```php
<?php
    /* Данные */
    $key = 'Это очень длинный ключ. Сильно больше, чем нужен шифру.';
    $plain_text = 'очень важные данные';

    /* Открываем модуль и создаём инициализирующий вектор */
    $td = mcrypt_module_open('des', '', 'ecb', '');
    $key = substr($key, 0, mcrypt_enc_get_key_size($td));
    $iv_size = mcrypt_enc_get_iv_size($td);
    $iv = mcrypt_create_iv($iv_size, MCRYPT_RAND);

    /* Инициализируем обработчик шифрования */
    if (mcrypt_generic_init($td, $key, $iv) != -1) {

        /* Шифруем данные */
        $c_t = mcrypt_generic($td, $plain_text);
        mcrypt_generic_deinit($td);

        /* Переинициализируем буферы для дешифровки */
        mcrypt_generic_init($td, $key, $iv);
        $p_t = mdecrypt_generic($td, $c_t);

        /* Убираем мусор */
        mcrypt_generic_deinit($td);
        mcrypt_module_close($td);
    }

    if (strncmp($p_t, $plain_text, strlen($plain_text)) == 0) {
        echo "ок\n";
    } else {
        echo "ошибка\n";
    }
?>
```

Приклад вище показує, як перевірити, що дані до шифрування збігаються з даними після дешифрування. Вкрай важливо переініціалізувати буфери шифрування за допомогою [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) перед дешифруванням даних.

Обробник дешифрування завжди має ініціалізуватися за допомогою [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) з ключем та ініціалізуючим вектором перед викликом функції. Як тільки шифрування завершено, необхідно звільнити буфери шифрування шляхом виклику функції [mcrypt\_generic\_deinit()](function.mcrypt-generic-deinit.md)Смотрите Приклад в описании функции[mcrypt\_module\_open()](function.mcrypt-module-open.md)

### Дивіться також

-   [mcrypt\_generic()](function.mcrypt-generic.md) \- Функція шифрує дані
-   [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) \- Функція ініціалізує всі буфери, необхідні для шифрування
-   [mcrypt\_generic\_deinit()](function.mcrypt-generic-deinit.md) \- Ця функція деініціалізує модуль шифрування
