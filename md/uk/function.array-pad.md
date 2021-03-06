- [«array_multisort](function.array-multisort.md)
- [array_pop »](function.array-pop.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Доповнити масив певним значенням до вказаної довжини

#array_pad

(PHP 4, PHP 5, PHP 7, PHP 8)

array_pad — Доповнити масив певним значенням до вказаної довжини

### Опис

**array_pad**(array `$array`, int `$length`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): array

Функція **array_pad()** повертає копію масиву `array`, доповненого
до розміру `length` елементами зі значенням `value`. Якщо параметр
`length` позитивний, то масив збільшується вправо, якщо негативний -
ліворуч. Якщо абсолютне значення параметра `length` менше або дорівнює
розміру масиву `array`, функція не здійснює жодних операцій. За один
раз можна додати максимум 1048576 елементів.

### Список параметрів

`array`
Вихідний масив, якого доповнюються елементи.

`length`
Новий розмір масиву.

`value`
Доповнюване значення, якщо довжина масиву `array` менше `length`.

### Значення, що повертаються

Повертає копію `array`, доповненого до розміру вказаного `length`
значенням `value`. Якщо параметр `length` позитивний, то масив
доповнюється праворуч, якщо він негативний - вліво. Якщо абсолютне
значення `length` менше або дорівнює довжині `array`, то додаток не
відбувається.

### Приклади

**Приклад #1 Приклад використання **array_pad()****

` <?php$input = array(12, 10, 9);$result = array_pad($input, 5, 0);// результат: array(12, 10, 9, 0, 0)$result = array_pad $input, -7, -1);// результат: array(-1, -1, -1, -1, 12, 10, 9)$result = array_pad($input, 2, "noop");/ / операція не зроблена `

### Дивіться також

- [array_fill()](function.array-fill.md) - Заповнює масив
значеннями
- [range()](function.range.md) - Створює масив, що містить діапазон
елементів
