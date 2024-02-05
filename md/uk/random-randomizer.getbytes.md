---
navigation:
  - random-randomizer.construct.md: '« Random\\Randomizer::\_\_construct'
  - random-randomizer.getbytesfromstring.md: 'Random\\Randomizer::getBytesFromString »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::getBytes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::getBytes

(PHP 8 >= 8.2.0)

Random\\Randomizer::getBytes — Отримує випадкові байти

### Опис

```methodsynopsis
public Random\Randomizer::getBytes(int $length): string
```

Створює рядок, що містить рівномірно вибрані випадкові байти із запитаною довжиною `length`

Оскільки байти, що повертаються, вибираються цілком випадково, отриманий рядок може містити недруковані символи або неприпустимі послідовності UTF-8. Перед передачею або відображенням може знадобитися її кодування.

### Список параметрів

`length`

Довжина випадкового рядка (string), який має бути повернутий, у байтах. Значення має бути більше чи одно

### Значення, що повертаються

Повертає рядок (string), що містить кількість кількості випадкових байтів.

### Помилки

-   Если значение параметра`length`меньше , буде викинута помилка [ValueError](class.valueerror.md)
-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Пример #1 Пример использования**Random\\Randomizer::getBytes()\*\*\*\*

```php
<?php

$r = new \Random\Randomizer();

echo bin2hex($r->getBytes(8)), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
ebdbe93cd56682c2
```

### Дивіться також

-   [random\_bytes()](function.random-bytes.md) \- Отримує криптографічно безпечні випадкові байти
-   [bin2hex()](function.bin2hex.md) \- Перетворює бінарні дані на шістнадцяткове подання
-   [base64\_encode()](function.base64-encode.md) \- Кодує дані у формат MIME base64
-   [Random\\Randomizer::getBytesFromString()](random-randomizer.getbytesfromstring.md) \- Отримує випадкові байти з вихідного рядка
