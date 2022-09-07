---
navigation:
  - language.namespaces.definition.md: « Определение пространств имён
  - language.namespaces.definitionmultiple.md: Опис кількох просторів імен в одному файлі »
  - index.md: PHP Manual
  - language.namespaces.md: Пространства имён
title: Визначення підпросторів імен
---
## Визначення підпросторів імен

(PHP 5> = 5.3.0, PHP 7, PHP 8)

Як файли і каталоги, простори імен PHP дозволяють створювати ієрархію імен. Таким чином, ім'я простору може бути визначене з підрівнями:

**Приклад #1 Визначення простору імен з ієрархією**

```php
<?php
namespace MyProject\Sub\Level;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

?>
```

Наведений вище приклад створює константу `MyProject\Sub\Level\CONNECT_OK`, клас `MyProject\Sub\Level\Connection` та функцію `MyProject\Sub\Level\connect`
