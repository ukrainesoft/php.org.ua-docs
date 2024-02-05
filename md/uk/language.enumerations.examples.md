---
navigation:
  - language.enumerations.object-differences.inheritance.md: « Чому перерахування не розширюються
  - language.errors.md: Помилки »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Приклади

**Приклад #1 Базові обмежені значення**

```php
<?php

enum SortOrder
{
    case Asc;
    case Desc;
}

function query($fields, $filter, SortOrder $order = SortOrder::Asc)
{
     /* ... */
}
?>
```

Функция`query()` тепер може безпечно працювати, знаючи, що параметр `$order` гарантовано буде або варіантом `SortOrder::Asc`, або варіантом `SortOrder::Desc`. Будь-яке інше значення призвело б до виключення [TypeError](class.typeerror.md)тому перевірка помилок або тестування не потрібні.

**Приклад #2 Розширені ексклюзивні значення**

```php
<?php

enum UserStatus: string
{
    case Pending = 'P';
    case Active = 'A';
    case Suspended = 'S';
    case CanceledByUser = 'C';

    public function label(): string
    {
        return match($this) {
            static::Pending => 'В ожидании',
            static::Active => 'Активный',
            static::Suspended => 'Приостановленный',
            static::CanceledByUser => 'Отменено пользователем',
        };
    }
}
?>
```

У цьому прикладі статус користувача може бути виключно одним із таких варіантів: `UserStatus::Pending` `UserStatus::Active` `UserStatus::Suspended`или`UserStatus::CanceledByUser`. Функція може ввести параметр `UserStatus` а потім прийняти тільки ці чотири значення, точка.

У всіх чотирьох значень є метод `label()`, який повертає рядок, що легко читається. Цей рядок не залежить від скалярного еквівалентного рядка "machine name", який можна використовувати, наприклад, у полі бази даних або значення випадаючого списку HTML.

```php
<?php

foreach (UserStatus::cases() as $case) {
    printf('<option value="%s">%s</option>\n', $case->value, $case->label());
}
?>
```
