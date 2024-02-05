---
navigation:
  - function.random-bytes.md: « random\_bytes
  - function.srand.md: srand »
  - index.md: PHP Manual
  - ref.random.md: Функції Random
title: random\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# random\_int

(PHP 7, PHP 8)

random\_int — Отримує криптографічно безпечне, рівномірно вибране ціле число

### Опис

```methodsynopsis
random_int(int $min, int $max): int
```

Створює рівномірно вибране ціле число між заданими мінімумом та максимумом.

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

`min`

Нижня межа діапазону.

`max`

Верхня межа діапазону.

### Значення, що повертаються

Криптографічно безпечне, рівномірно обране ціле число із замкнутого інтервалу \[`min` `max`\]. Можливими значеннями, що повертаються, є `min`и`max`

### Помилки

-   Якщо відповідних джерел випадкових величин відсутні, то викидається виняток[Random\\RandomException](class.random-randomexception.md)
-   Якщо поставити`max`меньше чем`min`, то буде викинуто виняток класу[ValueError](class.valueerror.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | У разі помилки CSPRNG, функція тепер буде викидати виняток [Random\\RandomException](class.random-randomexception.md). . Раніше викидався виняток [Exception](class.exception.md) |

### Приклади

**Пример #1 Пример использования**random\_int()\*\*\*\*

```php
<?php
var_dump(random_int(100, 999));
var_dump(random_int(-1000, 0));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(248)
int(-898)
```

### Дивіться також

-   [Random\\Randomizer::getInt()](random-randomizer.getint.md) \- Отримує рівномірно обране ціле число
-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
