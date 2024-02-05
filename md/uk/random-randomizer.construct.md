---
navigation:
  - class.random-randomizer.md: « Random\\Randomizer
  - random-randomizer.getbytes.md: 'Random\\Randomizer::getBytes »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::\_\_construct

(PHP 8 >= 8.2.0)

Random\\Randomizer::\_\_construct — Створює новий об'єкт Randomizer

### Опис

public**Random\\Randomizer::\_\_construct**(?[Random\\Engine](class.random-engine.md) `$engine` **`null`**) .

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`engine`

Класс[Random\\Engine](class.random-engine.md)який буде використовуватися для генерації випадкової послідовності.

Якщо параметр `engine`опущен или\*\*`null`\*\*, використовуватиметься об'єкт [Random\\Engine\\Secure](class.random-engine-secure.md)

### Приклади

**Пример #1 Пример использования**Random\\Randomizer::\_\_construct()\*\*\*\*

```php
<?php

/* ... */

?>
```

Висновок наведеного прикладу буде схожим на:

```
...
```
