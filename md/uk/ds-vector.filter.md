- [« Ds\Vector::count](ds-vector.count.md)
- [Ds\Vector :: find »](ds-vector.find.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Створює новий вектор із елементів, вибраних за допомогою заданої
callback-функції

# Ds\Vector::filter

(PECL ds \>= 1.0.0)

Ds\Vector::filter — Створює новий вектор із елементів, вибраних з
допомогою заданої callback-функції

### Опис

public **Ds\Vector::filter**([callable](language.types.callable.md)
`$callback` = ?): [Ds\Vector](class.ds-vector.md)

Створює новий вектор із елементів, вибраних за допомогою заданої
callback-функції.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): bool

Опціональний аргумент типу [callable](language.types.callable.md),
який повертає **`true`**, якщо значення має бути включене та
**`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи,
які наводяться до логічного значення **`true`** (дивіться
[приведення до boolean](language.types.boolean.md#language.types.boolean.casting)).

### Значення, що повертаються

Новий вектор, що містить значення, для яких функція callback
повернула **`true`**, або всі елементи, які при приведенні до
логічного типу стають **`true`**, якщо параметр `callback` не
заданий.

### Приклади

**Приклад #1 Приклад **Ds\Vector::filter()** з використанням
callback-функції**

` <?php$vector = new \Ds\Vector([1, 2, 3, 4, 5]);var_dump($vector->filter(function($value) {    return $value % 2 ==| ));?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Vector)#3 (2) {
[0]=>
int(2)
[1]=>
int(4)
}

**Приклад #2 Приклад **Ds\Vector::filter()** без callback-функції**

` <?php$vector = new \Ds\Vector([0, 1, 'a', true, false]);var_dump($vector->filter());?> `

Результатом виконання цього прикладу буде щось подібне:

object(Ds\Vector)#2 (3) {
[0]=>
int(1)
[1]=>
string(1) "a"
[2]=>
bool(true)
}
