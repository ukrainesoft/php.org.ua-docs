Константи перерахувань

-   [« Статические методы перечислений](language.enumerations.static-methods.html)
    
-   [Трейты »](language.enumerations.traits.html)
    
-   [PHP Manual](index.html)
    
-   [Перечисления](language.enumerations.html)
    
-   Константи перерахувань
    

## Константи перерахувань

Переліки можуть містити константи, які можуть бути загальнодоступними, закритими або захищеними, хоча практично закриті та захищені еквівалентні, оскільки успадкування не допускається.

Константа перерахування може належати до варіанта перерахування:

```php
<?php
enum Size
{
    case Small;
    case Medium;
    case Large;

    public const Huge = self::Large;
}
?>
```