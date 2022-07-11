- [« Серіалізація](language.enumerations.serialization.md)
- [Помилки »](language.errors.md)

- [PHP Manual](index.md)
- [Перерахування](language.enumerations.md)
- Приклади

## Приклади

**Приклад #1 Основні обмежені значення**

`<?phpenum SortOrder{   case ASC; case DESC;}function query($fields, $filter, SortOrder $order = SortOrder::ASC) { ... }?> `

Функція `query()` тепер може безпечно працювати, знаючи, що `$ order`
гарантовано буде або `SortOrder::ASC`, або `SortOrder::DESC`.
Будь-яке інше значення призвело до [TypeError](class.typeerror.md),
тому подальша перевірка помилок чи тестування не потрібна.

**Приклад #2 Розширені ексклюзивні значення**

`<?phpenum UserStatus: string{    case Pending = 'P'; case Active = 'A'; case Suspended = 'S'; case CanceledByUser = 'C'; public function label(): string    {        return match($this) {            static::Pending => 'В ожидании',            static::Active => 'Активный',            static::Suspended => 'Приостановленный',            static::CanceledByUser => 'Скасовано користувачем',         }; }}?> `

У цьому прикладі статус користувача може бути одним із таких:
`UserStatus::Pending`, `UserStatus::Active`, `UserStatus::Suspended` або
`UserStatus::CanceledByUser`. Функція може ввести параметр UserStatus
а потім прийняти тільки ці чотири значення, точка.

Усі чотири значення мають метод `label()`, який повертає
рядок, що читається. Цей рядок не залежить від скалярного еквівалентного рядка
"machine name", яку можна використовувати, наприклад, у полі бази даних
або поле вибору HTML.

` <?phpforeach (UserStatus::cases() as $case) {    printf('<option value="%s">%s</option>
', $case->value, $case->label());}?> `
