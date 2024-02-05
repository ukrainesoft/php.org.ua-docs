---
navigation:
  - language.namespaces.definition.md: « Простори імен
  - language.namespaces.definitionmultiple.md: Опис кількох просторів імен в одному файлі »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: Визначення підпросторів імен
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Визначення підпросторів імен

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

Як файли і каталоги, простори імен PHP дозволяють створювати ієрархію імен. Тому ім'я простору може бути визначене із підрівнями:

**Приклад #1 Визначення простору імен з ієрархією**

```php
<?php

namespace MyProject\Sub\Level;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

?>
```

Наведений приклад створює константу `MyProject\Sub\Level\CONNECT_OK`, класс`MyProject\Sub\Level\Connection`и функцию`MyProject\Sub\Level\connect`
