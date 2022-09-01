---
navigation:
  - language.namespaces.nested.md: « Определение подпространств имён
  - language.namespaces.basics.md: 'Використання простору імен: основи »'
  - index.md: PHP Manual
  - language.namespaces.md: Пространства имён
title: Опис кількох просторів імен в одному файлі
---
## Опис кількох просторів імен в одному файлі

(PHP 5> = 5.3.0, PHP 7, PHP 8)

Декілька просторів імен також можна описати в одному файлі за допомогою двох допустимих синтаксичних конструкцій.

**Приклад #1 Опис кількох просторів імен, простий синтаксис**

```php
<?php
namespace MyProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

namespace AnotherProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
?>
```

Цей синтаксис не рекомендується для комбінування просторів імен в одному файлі. Натомість рекомендується використовувати альтернативний синтаксис із дужками.

**Приклад #2 Опис кількох просторів імен, синтаксис із дужками**

```php
<?php
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace AnotherProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}
?>
```

Настійно не рекомендується під час програмування комбінувати декілька просторів імен в один файл. Основним застосуванням цього може бути поєднання декількох PHP-файлів в один файл.

Для об'єднання коду в глобальному просторі імен із кодом в інших просторах імен використовується тільки синтаксис із дужками. Глобальний код має бути поміщений у конструкцію опису простору імен без вказівки імені:

**Приклад #3 Опис глобального та звичайного простору імен в одному файлі**

```php
<?php
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace {       // глобальный код
session_start();
$a = MyProject\connect();
echo MyProject\Connection::start();
}
?>
```

PHP-код не може перебувати поза дужками конструкції простору імен, крім початкового виразу declare.

**Приклад #4 Опис глобального та звичайного простору імен в одному файлі**

```php
<?php
declare(encoding='UTF-8');
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace {      // глобальный код
session_start();
$a = MyProject\connect();
echo MyProject\Connection::start();
}
?>
```
