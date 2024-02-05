---
navigation:
  - language.enumerations.static-methods.md: « Статичні методи перерахувань
  - language.enumerations.traits.md: Трейти »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Константи перерахувань
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Константи перерахувань

До перерахунків дозволено включати константи із загальнодоступною, закритою або захищеною областю видимості, хоча на практиці закриті та захищені константи еквівалентні, оскільки успадкування не дозволене.

Константі перерахування можна посилатися на варіант перерахування:

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
