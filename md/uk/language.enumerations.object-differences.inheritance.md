---
navigation:
  - language.enumerations.serialization.md: « Серіалізація
  - language.enumerations.examples.md: Приклади »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Чому перерахування не розширюються
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Чому перерахування не розширюються

Для методів класів оголошено контракти:

```php
<?php

class A {}
class B extends A {}

function foo(A $a) {}

function bar(B $b) {
    foo($b);
}
?>
```

Цей код безпечний для типів, оскільки клас B виконує контракт класу A, і, за рахунок магії коваріантності та контраваріантності, очікування щодо методів будуть виправдані, за винятком винятків.

Переліки мають контракти на їх варіанти, а не методи:

```php
<?php

enum ErrorCode
{
    case SOMETHING_BROKE;
}

function quux(ErrorCode $errorCode)
{
    // Кажется, что этот код охватывает все варианты
    match ($errorCode) {
        ErrorCode::SOMETHING_BROKE => true,
    }
}

?>
```

Провівши статичний аналіз виразу [match](control-structures.match.md) у функції `quux`легко зрозуміти, що охоплений кожен варіант перерахування ErrorCode.

Але уявіть, що можна було б розширювати перерахування:

```php
<?php

// Экспериментальный код, в котором перечисления не конечно.
// Обратите внимание, что это не будет работать в PHP.
enum MoreErrorCode extends ErrorCode
{
    case PEBKAC;
}

function fot(MoreErrorCode $errorCode) {
    quux($errorCode);
}

fot(MoreErrorCode::PEBKAC);

?>
```

Дотримуючись стандартних правил успадкування, клас, який розширює інший клас, пройде перевірку типу.

Проблема полягає в тому, що вираз [match](control-structures.match.md) у функції `quux()` вже не покриває всіх випадків. Оскільки воно не знає про варіант `MoreErrorCode::PEBKAC`, вираз [match](control-structures.match.md) викине виняток.

Тому перерахування є остаточними і їх не дозволяється розширювати.
