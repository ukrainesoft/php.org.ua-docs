---
navigation:
  - language.enumerations.listing.md: « Список значень
  - language.enumerations.object-differences.inheritance.md: Чому перерахування не розширюються »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Серіалізація
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Серіалізація

Перерахування серіалізуються інакше, ніж об'єкти. Зокрема, у перерахувань є новий код серіалізації. `«E»`, Що вказує ім'я варіанта перерахування. Потім цей ідентифікатор буде доступний процедурі десеріалізації, щоб встановити змінну існуюче одноелементне значення. Це гарантує, що:

```php
<?php

Suit::Hearts === unserialize(serialize(Suit::Hearts));

print serialize(Suit::Hearts);
// E:11:"Suit:Hearts";
?>
```

Якщо при десеріалізації перерахування та варіант не будуть знайдені для порівняння серіалізованому значенню, буде видано попередження та повернуто **`false`**

Якщо чистий перелік серіалізується в JSON, буде видано помилку. Якщо типізований перелік серіалізується в JSON, він буде представлений лише його скалярним значенням типу, заданого у перерахуванні. Щоб перевизначити поведінку цих способів, реалізують інтерфейс [JsonSerializable](class.jsonserializable.md)

Для функції [print\_r()](function.print-r.md) висновок варіанта перерахування трохи відрізняється від об'єктів, щоб зменшити плутанину.

```php
<?php

enum Foo {
    case Bar;
}

enum Baz: int {
    case Beep = 5;
}

print_r(Foo::Bar);
print_r(Baz::Beep);

/* Выводит

Foo Enum (
    [name] => Bar
)
Baz Enum:int {
    [name] => Beep
    [value] => 5
}
*/
?>
```
