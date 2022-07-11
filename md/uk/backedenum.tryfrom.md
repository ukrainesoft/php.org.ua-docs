- [« BackedEnum::from](backedenum.from.md)
- [Контекстні опції та параметри »](context.md)

- [PHP Manual](index.md)
- [BackedEnum](class.backedenum.md)
- зіставляє скаляр з екземпляром перерахування або null

# BackedEnum::tryFrom

(PHP 8 \>= 8.1.0)

BackedEnum::tryFrom — Порівняє скаляр з екземпляром перерахунку або
null

### Опис

public static **BackedEnum::tryFrom**(int\|string `$value`): ?static

Метод **tryFrom()** переводить рядок (string) або число (int) в
відповідне значення перерахування, якщо є. Якщо
відповідне значення не визначено, чи повертається null.

### Список параметрів

`value`
Скалярне значення для порівняння з перерахуванням.

### Значення, що повертаються

Примірник перерахування або null, якщо екземпляр не знайдено.

### Приклади

**Приклад #1 Простий приклад використання**

У наведеному прикладі показано, як повертаються варіанти перерахування.

`<?phpenum Suit: string{   case Hearts = 'H'; case Diamonds = 'D'; case Clubs = 'C'; case Spades = 'S';}$h = Suit::tryFrom('H');var_dump($h);$b = Suit::tryFrom('B') ?? Suit::Spades;var_dump($b);?> `

Результат виконання цього прикладу:

enum(Suit::Hearts)
enum(Suit::Spades)

### Дивіться також

- [UnitEnum::cases()](unitenum.cases.md) - Повертає список
варіантів перерахування
- [BackedEnum::from()](backedenum.from.md) - Порівняє скаляр з
екземпляром перерахування
