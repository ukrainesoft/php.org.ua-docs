---
navigation:
  - function.rand.md: « rand
  - function.random-int.md: random\_int »
  - index.md: PHP Manual
  - ref.random.md: Функції Random
title: random\_bytes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# random\_bytes

(PHP 7, PHP 8)

random\_bytes — Отримує криптографічно безпечні випадкові байти

### Опис

```methodsynopsis
random_bytes(int $length): string
```

Створює рядок, що містить рівномірно вибрані випадкові байти із запитаною довжиною `length`

Оскільки байти, що повертаються, вибираються цілком випадково, отриманий рядок може містити недруковані символи або неприпустимі послідовності UTF-8. Перед передачею або відображенням може знадобитися її кодування.

Випадкова послідовність, що створюється функцією, підходить для всіх програм, включаючи генерацію довгострокових секретів, таких як ключі шифрування.

Джерела випадкових величин у порядку пріоритету:

-   Linux:[» getrandom()](http://man7.org/linux/man-pages/man2/getrandom.2.md), /dev/urandom
    
-   FreeBSD >= 12 (PHP >= 7.3): [» getrandom()](http://man7.org/linux/man-pages/man2/getrandom.2.md), /dev/urandom
    
-   Windows (PHP >= 7.2): [» CNG-API](https://docs.microsoft.com/en-us/windows/desktop/SecCNG/cng-portal)
    
    Windows:[» CryptGenRandom](https://msdn.microsoft.com/en-us/library/windows/desktop/aa379942(v=vs.85).aspx)
    
-   macOS (PHP >= 8.2; >= 8.1.9; >= 8.0.22, якщо CCRandomGenerateBytes доступний під час компіляції): CCRandomGenerateBytes()
    
    macOS (PHP >= 8.1; >= 8.0.2): arc4random\_buf(), /dev/urandom
    
-   NetBSD >= 7 (PHP >= 7.1; >= 7.0.1): arc4random\_buf(), /dev/urandom
    
-   OpenBSD >= 5.5 (PHP >= 7.1; >= 7.0.1): arc4random\_buf(), /dev/urandom
    
-   DragonflyBSD (PHP >= 8.1): [» getrandom()](http://man7.org/linux/man-pages/man2/getrandom.2.md), /dev/urandom
    
-   Solaris (PHP >= 8.1): [» getrandom()](http://man7.org/linux/man-pages/man2/getrandom.2.md), /dev/urandom
    
-   Будь-яка комбінація операційної системи та версії PHP, не вказана раніше: /dev/urandom
    
-   Якщо жодне з джерел не доступне або всі вони не генерують випадкову величину, то буде викинуто виняток[Random\\RandomException](class.random-randomexception.md)
    

> **Зауваження**: Ця функція була додана в PHP 7.0, а для версій з 5.2 до 5.6 включно доступна [» користувацька реалізація](https://github.com/paragonie/random_compat)

### Список параметрів

`length`

Довжина рядка, що генерується в байтах; повинно бути или больше.

### Значення, що повертаються

Повертає рядок, що складається із заданої кількості криптографічно безпечних байт.

### Помилки

-   Якщо відповідних джерел випадкових величин відсутні, то викидається виняток[Random\\RandomException](class.random-randomexception.md)
-   Если значение параметра`length`меньше , буде викинута помилка [ValueError](class.valueerror.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | У разі помилки CSPRNG, функція тепер буде викидати виняток [Random\\RandomException](class.random-randomexception.md). . Раніше викидався виняток [Exception](class.exception.md) |

### Приклади

**Пример #1 Пример использования**random\_bytes()\*\*\*\*

```php
<?php
$bytes = random_bytes(5);
var_dump(bin2hex($bytes));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(10) "385e33f741"
```

### Дивіться також

-   [Random\\Randomizer::getBytes()](random-randomizer.getbytes.md) \- Отримує випадкові байти
-   [random\_int()](function.random-int.md) \- Отримує криптографічно безпечне, рівномірно вибране ціле число
-   [bin2hex()](function.bin2hex.md) \- Перетворює бінарні дані на шістнадцяткове подання
-   [base64\_encode()](function.base64-encode.md) \- Кодує дані у формат MIME base64
