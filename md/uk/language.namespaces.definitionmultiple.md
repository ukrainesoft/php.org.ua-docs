---
navigation:
  - language.namespaces.nested.md: «Підпростору імен
  - language.namespaces.basics.md: Основи »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: Опис кількох просторів імен в одному файлі
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Опис кількох просторів імен в одному файлі

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

В одному файлі можна оголошувати кілька просторів імен. Є два дозволені синтаксиси:

**Приклад #1 Опис кількох просторів імен, простий синтаксис**

```php
<?php

namespace MyProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

namespace AnotherProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

?>
```

Цей синтаксис не рекомендований для комбінування простір імен в одному файлі. Натомість краще користуватися альтернативним синтаксисом зі дужками.

**Приклад #2 Опис кількох просторів імен, синтаксис із дужками**

```php
<?php

namespace MyProject {
    const CONNECT_OK = 1;
    class Connection { /* ... */ }
    function connect() { /* ... */  }
}

namespace AnotherProject {
    const CONNECT_OK = 1;
    class Connection { /* ... */ }
    function connect() { /* ... */  }
}

?>
```

Настійно не рекомендовано під час програмування комбінувати кілька просторів імен в один файл. Основний сценарій того, коли це може знадобитися - об'єднання декількох PHP-файлів в один файл.

Для об'єднання коду в глобальному просторі імен з кодом в інших просторах імен користуються тільки синтаксисом з дужками. Глобальний код має бути поміщений у конструкцію опису простору імен без вказівки імені:

**Приклад #3 Опис глобального та звичайного простору імен в одному файлі**

```php
<?php

namespace MyProject {
    const CONNECT_OK = 1;
    class Connection { /* ... */ }
    function connect() { /* ... */  }
}

namespace {       // глобальный код
    session_start();
    $a = MyProject\connect();
    echo MyProject\Connection::start();
}

?>
```

PHP-код не може перебувати поза дужками конструкції простору імен, крім початкового виразу declare.

**Приклад #4 Опис глобального та звичайного простору імен в одному файлі**

```php
<?php

declare(encoding='UTF-8');
namespace MyProject {
    const CONNECT_OK = 1;
    class Connection { /* ... */ }
    function connect() { /* ... */  }
}

namespace {      // глобальный код
    session_start();
    $a = MyProject\connect();
    echo MyProject\Connection::start();
}

?>
```
