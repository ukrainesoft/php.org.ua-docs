- [« Ds\Vector::push](ds-vector.push.md)
- [Ds\Vector::remove »](ds-vector.remove.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Зменшує вектор до одного значення, використовуючи callback-функцію

# Ds\Vector::reduce

(PECL ds \>= 1.0.0)

Ds\Vector::reduce — Зменшує вектор до одного значення, використовуючи
callback-функцію

### Опис

public **Ds\Vector::reduce**([callable](language.types.callable.md)
`$callback`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$initial` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Сплескує вектор до одного значення, використовуючи callback-функцію.

### Список параметрів

`callback`
callback([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$carry`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

`carry`
Значення, повернене попереднім запуском функції або initial, якщо
функція запущена вперше.

`value`
Значення поточної ітерації.

`initial`
Початкове значення параметра carry. Можна вказати **`null`**.

### Значення, що повертаються

Значення повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::reduce()** з початковим
значенням**

` <?php$vector = new \Ds\Vector([1, 2, 3]);$callback = function($carry, $value) {    return $carry * $value;};var_dump($ ($callback, 5));// Iterations://// $carry = $initial = 5//// $carry = $carry * 1 =  5// $carry = $carry * 2 = $ carry = $carry * 3 = 30?> `

Результатом виконання цього прикладу буде щось подібне:

int(30)

**Приклад #2 Приклад використання **Ds\Vector::reduce()** без початкового
значення**

` <?php$vector = new \Ds\Vector([1, 2, 3]);var_dump($vector->reduce(function($carry, $value) {    return $carry + $value + ) );// Iterations://// $carry = $initial = null//// $carry = $carry + 1 + 5 =  6// $carry = $carry + 2 + $ $carry + 3 + 5 = 21?> `

Результатом виконання цього прикладу буде щось подібне:

int(21)
