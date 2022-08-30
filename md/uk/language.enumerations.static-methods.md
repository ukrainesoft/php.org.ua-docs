Статичні методи перерахувань

-   [« Методи перерахувань](language.enumerations.methods.md)
    
-   [Константи перерахувань »](language.enumerations.constants.md)
    
-   [PHP Manual](index.md)
    
-   [Перечисления](language.enumerations.md)
    
-   Статичні методи перерахувань
    

## Статичні методи перерахувань

Переліки можуть мати статичні методи. Використання статичних методів у перерахуванні насамперед призначено для альтернативних конструкторів. Наприклад:

```php
<?php
enum Size
{
    case Small;
    case Medium;
    case Large;

    public static function fromLength(int $cm): static
    {
        return match(true) {
            $cm < 50 => static::Small,
            $cm < 100 => static::Medium,
            default => static::Large,
        };
    }
}
?>
```

Статичні методи можуть бути загальнодоступними, закритими або захищеними, хоча на практиці закриті та захищені еквівалентні, оскільки успадкування не допускається.