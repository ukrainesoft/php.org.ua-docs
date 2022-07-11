- [« Ds\Set::merge](ds-set.merge.md)
- [Ds\Set::remove »](ds-set.remove.md)

- [PHP Manual](index.md)
- [Набір](class.ds-set.md)
- Зменшує колекцію до одного значення, використовуючи callback-функцію

# Ds\Set::reduce

(PECL ds \>= 1.0.0)

Ds\Set::reduce — Зменшує колекцію до одного значення, використовуючи
callback-функцію

### Опис

public **Ds\Set::reduce**([callable](language.types.callable.md)
`$callback`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$initial` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Зменшує колекцію до одного значення, використовуючи callback-функцію.

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

Значення, повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **Ds\Set::reduce()** з початковим
значенням**

` <?php$set = new \Ds\Set([1, 2, 3]);$callback = function($carry, $value) {    return $carry * $value;};var_dump($set ($callback, 5));// Ітерації://// $carry = $initial = 5//// $carry = $carry * 1 =  5// $carry = $carry * 2 = carry = $carry * 3 = 30?> `

Результатом виконання цього прикладу буде щось подібне:

int(30)

**Приклад #2 Приклад використання **Ds\Set::reduce()** без початкового
значення**

` <?php$set = new \Ds\Set([1, 2, 3]);var_dump($set->reduce(function($carry, $value) {   return $carry + $value + 5); );// Ітерації://// $carry = $initial = null//// $carry = $carry + 1 + 5 =  6// $carry = $carry + 2 + $ $carry + 3 + 5 = 21?> `

Результатом виконання цього прикладу буде щось подібне:

int(21)
