Приклади

-   [« Сериализация](language.enumerations.serialization.html)
    
-   [Ошибки »](language.errors.html)
    
-   [PHP Manual](index.html)
    
-   [Перечисления](language.enumerations.html)
    
-   Приклади
    

## Приклади

**Приклад #1 Основні обмежені значення**

```php
<?php
enum SortOrder
{
    case ASC;
    case DESC;
}

function query($fields, $filter, SortOrder $order = SortOrder::ASC) { ... }
?>
```

Функція `query()` тепер може безпечно працювати, знаючи, що `$order` гарантовано буде або `SortOrder::ASC`, або `SortOrder::DESC`. Будь-яке інше значення призвело б до [TypeError](class.typeerror.html)тому подальша перевірка помилок або тестування не потрібна.

**Приклад #2 Розширені ексклюзивні значення**

```php
<?php
enum UserStatus: string
{
    case Pending = 'P';
    case Active = 'A';
    case Suspended = 'S';
    case CanceledByUser = 'C';

    public function label(): string
    {
        return match($this) {
            static::Pending => 'В ожидании',
            static::Active => 'Активный',
            static::Suspended => 'Приостановленный',
            static::CanceledByUser => 'Отменено пользователем',
        };
    }
}
?>
```

У цьому прикладі статус користувача може бути одним із таких: `UserStatus::Pending` `UserStatus::Active` `UserStatus::Suspended` або `UserStatus::CanceledByUser`. Функція може ввести параметр `UserStatus` а потім прийняти тільки ці чотири значення, точка.

У всіх чотирьох значень є метод `label()`, який повертає рядок, що читається. Цей рядок не залежить від скалярного еквівалентного рядка "machine name", який можна використовувати, наприклад, у полі бази даних або полі вибору HTML.

```php
<?php
foreach (UserStatus::cases() as $case) {
    printf('<option value="%s">%s</option>\n', $case->value, $case->label());
}
?>
```