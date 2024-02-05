---
navigation:
  - class.random-engine-secure.md: « Random\\Engine\\Secure
  - class.random-engine-mt19937.md: Random\\Engine\\Mt19937 »
  - index.md: PHP Manual
  - class.random-engine-secure.md: Random\\Engine\\Secure
title: 'Random\\Engine\\Secure::generate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\Secure::generate

(PHP 8 >= 8.2.0)

Random\\Engine\\Secure::generate — Створює криптографічно безпечну випадкову послідовність

### Опис

```methodsynopsis
public Random\Engine\Secure::generate(): string
```

Повертає криптографічно безпечну випадкову послідовність.

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
    

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що містить **`PHP_INT_SIZE`** криптографічно захищених випадкових байтів.

### Помилки

-   Якщо відповідних джерел випадкових величин відсутні, то викидається виняток[Random\\RandomException](class.random-randomexception.md)
