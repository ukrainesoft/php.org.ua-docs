- [«array_search](function.array-search.md)
- [array_slice »](function.array-slice.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Витягує перший елемент масиву

#array_shift

(PHP 4, PHP 5, PHP 7, PHP 8)

array_shift — Витягує перший елемент масиву

### Опис

**array_shift**(array `&$array`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

**array_shift()** отримує перше значення масиву `array` і повертає
його, скорочуючи розмір `array` на один елемент. Усі числові ключі будуть
змінені таким чином, що нумерація масиву почнеться з нуля,
час як рядкові ключі залишаться незмінними.

> **Примітка**: Ця функція під час дзвінка
> [скидає](function.reset.md) покажчик масиву, переданого
> параметром.

### Список параметрів

`array`
Вхідний масив.

### Значення, що повертаються

Повертає видобуте значення або **`null`**, якщо `array` порожній чи не
є масивом.

### Приклади

**Приклад #1 Приклад використання **array_shift()****

` <?php$stack = array("orange", "banana", "apple", "raspberry");$fruit = array_shift($stack);print_r($stack);?> `

Результат виконання цього прикладу:

Array
(
[0] => banana
[1] => apple
[2] => raspberry
)

і значення `orange` буде присвоєно змінній `$fruit`.

### Дивіться також

- [array_unshift()](function.array-unshift.md) - Додає один або
кілька елементів на початок масиву
- [array_push()](function.array-push.md) - Додає один або
кілька елементів у кінець масиву
- [array_pop()](function.array-pop.md) - Витягує останній елемент
масиву
