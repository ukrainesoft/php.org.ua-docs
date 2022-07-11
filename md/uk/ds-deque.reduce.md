- [« Ds\Deque::push](ds-deque.push.md)
- [Ds\Deque::remove »](ds-deque.remove.md)

- [PHP Manual](index.md)
- [Двостороння черга](class.ds-deque.md)
- Зменшує колекцію до одного значення, використовуючи callback-функцію

# Ds\Deque::reduce

(PECL ds \>= 1.0.0)

Ds\Deque::reduce — Зменшує колекцію до одного значення, використовуючи
callback-функцію

### Опис

public **Ds\Deque::reduce**([callable](language.types.callable.md)
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
функцію запущено вперше.

`value`
Значення поточної ітерації.

`initial`
Початкове значення параметра carry. Можна вказати **`null`**.

### Значення, що повертаються

Значення, повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **Ds\Deque::reduce()** з початковим
значенням**

` <?php$deque = new \Ds\Deque([1, 2, 3]);$callback = function($carry, $value) {    return $carry * $value;};var_dump($ ($callback, 5));// Iterations://// $carry = $initial = 5//// $carry = $carry * 1 =  5// $carry = $carry * 2 = $ carry = $carry * 3 = 30?> `

Результатом виконання цього прикладу буде щось подібне:

int(30)

**Приклад #2 Приклад використання **Ds\Deque::reduce()** без початкового
значення**

` <?php$deque = new \Ds\Deque([1, 2, 3]);var_dump($deque->reduce(function($carry, $value) {    return $carry + $value + ) );// Iterations://// $carry = $initial = null//// $carry = $carry + 1 + 5 =  6// $carry = $carry + 2 + $ $carry + 3 + 5 = 21?> `

Результатом виконання цього прикладу буде щось подібне:

int(21)
