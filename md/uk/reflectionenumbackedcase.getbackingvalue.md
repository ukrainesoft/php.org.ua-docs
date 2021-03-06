- [« ReflectionEnumBackedCase::\_\_construct](reflectionenumbackedcase.construct.md)
- [ReflectionZendExtension »](class.reflectionzendextension.md)

- [PHP Manual](index.md)
- [ReflectionEnumBackedCase](class.reflectionenumbackedcase.md)
- Отримує скалярне значення варіанта перерахування

# ReflectionEnumBackedCase::getBackingValue

(PHP 8 \>= 8.1.0)

ReflectionEnumBackedCase::getBackingValue — Отримує скалярне значення
варіанти перерахування

### Опис

public **ReflectionEnumBackedCase::getBackingValue**(): int\|string

Отримує скалярне значення варіанта перерахування.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Скалярне значення варіанта перерахування.

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::getBackingValue()****

`<?phpenum Suit: string{   case Hearts = 'H'; case Diamonds = 'D'; case Clubs = 'C'; case Spades = 'S';}$rEnum = new ReflectionEnum(Suit::class);$rCase = $rEnum->getCase('Spades');var_dump($rCase->getBackingValue());?> `

Результат виконання цього прикладу:

string(1) "S"

### Дивіться також

- [Перерахування](language.enumerations.md)
