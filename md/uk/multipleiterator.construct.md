- [« MultipleIterator::attachIterator](multipleiterator.attachiterator.md)
- [MultipleIterator::containsIterator »](multipleiterator.containsiterator.md)

- [PHP Manual](index.md)
- [MultipleIterator](class.multipleiterator.md)
- Створює новий MultipleIterator

# MultipleIterator::\_\_construct

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

MultipleIterator::\_\_construct — Створює новий MultipleIterator

### Опис

public **MultipleIterator::\_\_construct**(int `$flags` =
MultipleIterator::MIT_NEED_ALL \| MultipleIterator::MIT_KEYS_NUMERIC)

Створює новий MultipleIterator.

### Список параметрів

`flags`
Прапори для установки, відповідно до [Предвизначеним константам](class.multipleiterator.md#multipleiterator.constants).

- **`MultipleIterator::MIT_NEED_ALL`** або
**`MultipleIterator::MIT_NEED_ANY`**
- **`MultipleIterator::MIT_KEYS_NUMERIC`** або
**`MultipleIterator::MIT_KEYS_ASSOC`**

За замовчуванням
**`MultipleIterator::MIT_NEED_ALL`**\|**`MultipleIterator::MIT_KEYS_NUMERIC`**.

### Приклади

**Приклад #1 Ітерування MultipleIterator**

` <?php$people = new ArrayIterator(array('John', 'Jane', 'Jack', 'Judy'));$roles = new ArrayIterator(array('Developer', Scrum '));$team = new MultipleIterator($flags);$team->attachIterator($people, 'person');$team->attachIterator($roles, 'role');foreach ($team as $member) {   print_r($member);}?> `

Висновок з $flags = MIT_NEED_ALL|MIT_KEYS_NUMERIC`

Array
(
[0] => John
[1] => Developer
)
Array
(
[0] => Jane
[1] => Scrum Master
)
Array
(
[0] => Jack
[1] => Project Owner
)

Висновок з $flags = MIT_NEED_ANY|MIT_KEYS_NUMERIC`

Array
(
[0] => John
[1] => Developer
)
Array
(
[0] => Jane
[1] => Scrum Master
)
Array
(
[0] => Jack
[1] => Project Owner
)
Array
(
[0] => Judy
[1] =>
)

Висновок з $flags = MIT_NEED_ALL | MIT_KEYS_ASSOC

Array
(
[person] => John
[Role] => Developer
)
Array
(
[person] => Jane
[Role] => Scrum Master
)
Array
(
[person] => Jack
[Role] => Project Owner
)

Висновок з $flags = MIT_NEED_ANY | MIT_KEYS_ASSOC

Array
(
[person] => John
[Role] => Developer
)
Array
(
[person] => Jane
[Role] => Scrum Master
)
Array
(
[person] => Jack
[Role] => Project Owner
)
Array
(
[person] => Judy
[role] =>
)

### Дивіться також

- [Предвизначені константи](class.multipleiterator.md#multipleiterator.constants)
- [MultipleIterator::valid()](multipleiterator.valid.md) - Перевіряє
коректність підитераторів
