---
navigation:
  - random-randomizer.getbytes.md: '« Random\\Randomizer::getBytes'
  - random-randomizer.getfloat.md: 'Random\\Randomizer::getFloat »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::getBytesFromString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::getBytesFromString

(PHP 8 >= 8.3.0)

Random\\Randomizer::getBytesFromString — Отримує випадкові байти з вихідного рядка

### Опис

```methodsynopsis
public Random\Randomizer::getBytesFromString(string $string, int $length): string
```

Генерує із вхідного рядка `string` рядок, що містить рівномірно вибрані випадкові байти заданим параметром `length` довжини.

Імовірність вибору байта пропорційна його частці у вхідному рядку `string`. Якщо кожен байт зустрічається однакову кількість разів, можливість вибору кожного байта буде однаковою.

### Список параметрів

`string`

Рядок (string), з якого вибираються байти, що повертаються.

`length`

Довжина випадкового рядка (string) у байтах, яка має бути повернена; повинна дорівнювати или больше.

### Значення, що повертаються

Повертає рядок (string), що містить кількість кількості випадкових байтів, взятих з вхідного рядка. `string`

### Помилки

-   Якщо параметр `string`порожній, буде викинуто виняток[ValueError](class.valueerror.md)
-   Якщо значення довжини`length`меньше , буде викинуто виняток [ValueError](class.valueerror.md)
-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Пример #1 Пример использования метода**Random\\Randomizer::getBytesFromString()\*\*\*\*

```php
<?php

$randomizer = new \Random\Randomizer();

printf(
    "%s.example.com",
    $randomizer->getBytesFromString('abcdefghijklmnopqrstuvwxyz0123456789', 16)
);
?>
```

Висновок наведеного прикладу буде схожим на:

```
3zsw04eiubcf82jd.example.com
```

**Приклад #2 Приклад генерації випадкового коду багатофакторної аутентифікації**

```php
<?php

// Движок Secure установлен по умолчанию, но укажем его явно, потому что
// многофакторные коды чувствительны к безопасности.
$randomizer = new \Random\Randomizer(new \Random\Engine\Secure());

echo implode('-', str_split($randomizer->getBytesFromString('0123456789', 20), 5));
?>
```

Висновок наведеного прикладу буде схожим на:

```
11551-80418-27047-42075
```

**Приклад #3 Приклад вибору рядка з нерівномірним розподілом**

```php
<?php

$randomizer = new \Random\Randomizer();

echo $randomizer->getBytesFromString('aaaaabcdef', 20);
?>
```

Висновок наведеного прикладу буде схожим на:

```
fddacbeaaeaaacaaaaca
```

### Дивіться також

-   [Random\\Randomizer::getBytes()](random-randomizer.getbytes.md) \- Отримує випадкові байти
