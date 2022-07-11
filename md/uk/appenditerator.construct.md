- [« AppendIterator::append](appenditerator.append.md)
- [AppendIterator::current »](appenditerator.current.md)

- [PHP Manual](index.md)
- [AppendIterator](class.appenditerator.md)
- Створює AppendIterator

# AppendIterator::\_\_construct

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

AppendIterator::\_\_construct — Створює AppendIterator

### Опис

public **AppendIterator::\_\_construct**()

Створює AppendIterator.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Ітерація AppendIterator за допомогою foreach**

` <?php$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Oliv 'Ham'));$appendIterator = new AppendIterator;$appendIterator->append($pizzas);$appendIterator->append($toppings);foreach ($appendIterator as $key => $item) {          ' => ' . $item . PHP_EOL;}?> `

Результат виконання цього прикладу:

0 => Margarita
1 => Siciliana
2 => Hawaii
0 => Cheese
1 => Anchovies
2 => Olives
3 => Pineapple
4 => Ham

**Приклад #2 Ітерація AppendIterator за допомогою AppendIterator API**

` <?php$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Oliv 'Ham'));$appendIterator = new AppendIterator;$appendIterator->append($pizzas);$appendIterator->append($toppings);while ($appendIterator->valid()|                                             | %s => %s%s',   $appendIterator->getIteratorIndex(),        $appendIterator->key(),        $appendItera     $appendIterator->next();}?> `

Результат виконання цього прикладу:

0 => 0 => Margarita
0 => 1 => Siciliana
0 => 2 => Hawaii
1 => 0 => Cheese
1 => 1 => Anchovies
1 => 2 => Olives
1 => 3 => Pineapple
1 => 4 => Ham

### Примітки

**Застереження**

При використанні функції
[iterator_to_array()](function.iterator-to-array.md) для копіювання
значення AppendIterator в масив, вам необхідно встановити
додатковий аргумент `use_key` на значення **`false`**. Коли
`use_key` не приймає значення **`false`**, будь-які ключі, повторно
що зустрічаються у внутрішніх ітераторах, будуть перезаписані в
масив, що повертається. Зберегти оригінальні ключі неможливо.

### Дивіться також

- [AppendIterator::append()](appenditerator.append.md) - Додає
ітератор
