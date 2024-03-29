---
navigation:
  - language.namespaces.rationale.md: « Огляд
  - language.namespaces.nested.md: Підпростори імен »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: Визначення просторів імен
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Визначення просторів імен

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

Хоча будь-який коректний PHP-код може знаходитися всередині простору імен, тільки класи (включаючи абстрактні та трейти), інтерфейси, функції та константи залежать від нього.

Простір імен оголошують, вказуючи зарезервоване слово `namespace`. Простір імен у файлах оголошують на початку, перед будь-яким іншим кодом, крім зарезервованого слова [declare](control-structures.declare.md)

**Приклад #1 Оголошення єдиного простору імен**

```php
<?php

namespace MyProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

?>
```

> **Зауваження**: Абсолютні імена (тобто імена, які починаються зі зворотної косою межі) не допускаються в оголошеннях простору імен, оскільки такі конструкції інтерпретуються як відносні вирази простору імен.

Тільки виразу `declare` дозволено перебувати перед оголошенням простору імен, щоб визначити кодування вихідного файлу. Крім сказаного, перед оголошенням простору імен не повинно бути іншого коду, ніж PHP-код, включаючи зайві прогалини:

**Приклад #2 Оголошення простого простору імен**

```php
<html>
<?php

namespace MyProject; // fatal error — объявление пространства имён должно быть первым выражением в скрипте

?>
```

Крім того, той самий простір імен, на відміну від інших конструкцій PHP, можна визначати в декількох файлах, що допомагає розподіляти їх зміст по файловій системі.
