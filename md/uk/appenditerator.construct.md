Створює AppendIterator

-   [« AppendIterator::append](appenditerator.append.html)
    
-   [AppendIterator::current »](appenditerator.current.html)
    
-   [PHP Manual](index.html)
    
-   [AppendIterator](class.appenditerator.html)
    
-   Створює AppendIterator
    

# AppendIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

AppendIterator::construct — Створює AppendIterator

### Опис

public **AppendIterator::construct**

Створює AppendIterator.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Ітерація AppendIterator за допомогою foreach**

```php
<?php
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

foreach ($appendIterator as $key => $item) {
    echo $key . ' => ' . $item . PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
0 => Margarita
1 => Siciliana
2 => Hawaii
0 => Cheese
1 => Anchovies
2 => Olives
3 => Pineapple
4 => Ham
```

**Приклад #2 Ітерація AppendIterator за допомогою AppendIterator API**

```php
<?php
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

while ($appendIterator->valid()) {
    printf(
        '%s => %s => %s%s',
        $appendIterator->getIteratorIndex(),
        $appendIterator->key(),
        $appendIterator->current(),
        PHP_EOL
    );
    $appendIterator->next();
}
?>
```

Результат виконання цього прикладу:

```
0 => 0 => Margarita
0 => 1 => Siciliana
0 => 2 => Hawaii
1 => 0 => Cheese
1 => 1 => Anchovies
1 => 2 => Olives
1 => 3 => Pineapple
1 => 4 => Ham
```

### Примітки

**Застереження**

При використанні функції [iteratorтоarray()](function.iterator-to-array.html) Для копіювання значення AppendIterator в масив вам необхідно встановити додатковий аргумент `use_key` на значення **`false`**. Коли `use_key` не набуває значення **`false`**, якісь ключі, що повторно зустрічаються у внутрішніх ітераторах, будуть перезаписані в масив, що повертається. Зберегти оригінальні ключі неможливо.

### Дивіться також

-   [AppendIterator::append()](appenditerator.append.html) - додає ітератор