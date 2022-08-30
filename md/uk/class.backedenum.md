Інтерфейс BackedEnum

-   [« UnitEnum::cases](unitenum.cases.html)
    
-   [BackedEnum::from »](backedenum.from.html)
    
-   [PHP Manual](index.html)
    
-   [Вбудовані інтерфейси та класи](reserved.interfaces.html)
    
-   Інтерфейс BackedEnum
    

# Інтерфейс BackedEnum

(PHP 8> = 8.1.0)

## Вступ

Інтерфейс **BackedEnum** автоматично застосовується двигуном до типізованих перерахувань. Він не може бути реалізований користувачами класами. Перерахування що неспроможні перевизначати його способи, оскільки продажу за замовчуванням надаються движком. Доступний лише для перевірки типу.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     interface BackedEnum
      extends
       UnitEnum
     
     {

    /* Методы */
    
   public static from(int|string $value): static
public static tryFrom(int|string $value): ?static


    /* Наследуемые методы */
    public static UnitEnum::cases(): array

   }
```

## Зміст

-   [BackedEnum::from](backedenum.from.html) - Зіставляє скаляр з екземпляром перерахування
-   [BackedEnum::tryFrom](backedenum.tryfrom.html) — Порівнює скаляр з екземпляром перерахування чи null