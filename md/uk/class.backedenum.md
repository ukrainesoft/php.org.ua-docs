---
navigation:
  - unitenum.cases.md: '« UnitEnum::cases'
  - backedenum.from.md: 'BackedEnum::from »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс BackedEnum
---
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

-   [BackedEnum::from](backedenum.from.md) - Зіставляє скаляр з екземпляром перерахування
-   [BackedEnum::tryFrom](backedenum.tryfrom.md) — Порівнює скаляр з екземпляром перерахування чи null
