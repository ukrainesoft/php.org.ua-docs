---
navigation:
  - stringable.tostring.md: '« Stringable::toString'
  - unitenum.cases.md: 'UnitEnum::cases »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс UnitEnum
---
# Інтерфейс UnitEnum

(PHP 8> = 8.1.0)

## Вступ

Інтерфейс **UnitEnum** автоматично застосовується двигуном до всіх перерахувань. Він не може бути реалізований користувачами класами. Перерахування що неспроможні перевизначати його способи, оскільки продажу за замовчуванням надаються движком. Доступний лише для перевірки типу.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface UnitEnum {

    /* Методы */
    
   public static cases(): array

   }
```

## Зміст

-   [UnitEnum::cases](unitenum.cases.md) — Повертає перелік варіантів перерахування
