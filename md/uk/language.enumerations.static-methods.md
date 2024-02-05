---
navigation:
  - language.enumerations.methods.md: « Методи перерахувань
  - language.enumerations.constants.md: Константи перерахувань »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Статичні методи перерахувань
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Статичні методи перерахувань

У переліках можна оголошувати статичні способи. Статичні методи у перерахуванні насамперед виступають у ролі альтернативних конструкторів. Наприклад:

```php
<?php

enum Size
{
    case Small;
    case Medium;
    case Large;

    public static function fromLength(int $cm): static
    {
        return match(true) {
            $cm < 50 => static::Small,
            $cm < 100 => static::Medium,
            default => static::Large,
        };
    }
}
?>
```

Статичні методи дозволено оголошувати загальнодоступними, закритими чи захищеними, хоча практично закриті і захищені методи еквівалентні, оскільки успадкування не дозволено.
