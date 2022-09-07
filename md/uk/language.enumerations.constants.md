---
navigation:
  - language.enumerations.static-methods.md: « Статичні методи перерахувань
  - language.enumerations.traits.md: Трейти »
  - index.md: PHP Manual
  - language.enumerations.md: Перечисления
title: Константи перерахувань
---
## Константи перерахувань

Переліки можуть містити константи, які можуть бути загальнодоступними, закритими або захищеними, хоча практично закриті та захищені еквівалентні, оскільки успадкування не допускається.

Константа перерахування може належати до варіанта перерахування:

```php
<?php
enum Size
{
    case Small;
    case Medium;
    case Large;

    public const Huge = self::Large;
}
?>
```
