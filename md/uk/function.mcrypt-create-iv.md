Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела

-   [« Mcrypt](ref.mcrypt.html)
    
-   [mcryptdecrypt »](function.mcrypt-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела
    

# mcryptcreateверб

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptcreateiv — Створити вектор, що ініціалізує (Initialization Vector або IV) з випадкового джерела

**Увага**

Ця функція оголошена *застарілої* в PHP 7.1.0 та *ВИДАЛЕНО* у PHP 7.2.0.

Є такі альтернативи:

-   [randombytes()](function.random-bytes.html)

### Опис

```methodsynopsis
mcrypt_create_iv(int $size, int $source = MCRYPT_DEV_URANDOM): string
```

Створює вектор, що ініціалізує, з випадкового джерела.

IV призначений лише завдання альтернативного початкового випадкового числа для процедур шифрування. IV не обов'язково має бути секретним, хоча це й бажано. Ви навіть можете відправити його разом зі своїм зашифрованим текстом, не втрачаючи при цьому безпеки.

### Список параметрів

`size`

Розмір ІV.

`source`

Джерело IV. Джерело може бути задане однією з констант: **`MCRYPT_RAND`** (Системний генератор випадкових чисел), **`MCRYPT_DEV_RANDOM`** (читає дані з /dev/random) або **`MCRYPT_DEV_URANDOM`** (читає дані із /dev/urandom). До версії 5.3.0 на Windows підтримувався тільки **`MCRYPT_RAND`**

Зверніть увагу, що до PHP 5.6.0 значення за промовчанням було **`MCRYPT_DEV_RANDOM`**

> **Зауваження**: Зверніть увагу, що **`MCRYPT_DEV_RANDOM`** може блокуватися до появи достатньої ентропії.

### Значення, що повертаються

Повертає вектор, що ініціалізує, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mcryptcreateiv()****

```php
<?php
    $size = mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB);
    $iv = mcrypt_create_iv($size, MCRYPT_DEV_RANDOM);
?>
```

### Дивіться також

-   [» http://www.ciphersbyritter.com/GLOSSARY.HTM#IV](http://www.ciphersbyritter.com/GLOSSARY.HTM#IV)
-   [» http://www.quadibloc.com/crypto/co0409.htm](http://www.quadibloc.com/crypto/co0409.htm)
-   Applied Cryptography by Schneier (ISBN 0-471-11709-9), розділ 9.3
-   [randombytes()](function.random-bytes.html) - Генерує криптографічно безпечні псевдовипадкові байти