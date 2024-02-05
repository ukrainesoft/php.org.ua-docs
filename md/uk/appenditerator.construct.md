---
navigation:
  - appenditerator.append.md: '« AppendIterator::append'
  - appenditerator.current.md: 'AppendIterator::current »'
  - index.md: PHP Manual
  - class.appenditerator.md: AppendIterator
title: 'AppendIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# AppendIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

AppendIterator::\_\_construct — Створює AppendIterator

### Опис

public **AppendIterator::\_\_construct**()

Створює AppendIterator.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Ітерація AppendIterator за допомогою foreach**

```php
<?php
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

foreach ($appendIterator as $key => $item) {
    echo $key . ' => ' . $item . PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

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
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

while ($appendIterator->valid()) {
    printf(
        '%s => %s => %s%s',
        $appendIterator->getIteratorIndex(),
        $appendIterator->key(),
        $appendIterator->current(),
        PHP_EOL
    );
    $appendIterator->next();
}
?>
```

Результат виконання наведеного прикладу:

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

При использовании функции[iterator\_to\_array()](function.iterator-to-array.md) Для копіювання значення AppendIterator в масив вам необхідно встановити додатковий аргумент `use_key`в значение\*\*`false`**Когда`use_key`не принимает значение**`false`\*\*, якісь ключі, що повторно зустрічаються у внутрішніх ітераторах, будуть перезаписані в масив, що повертається. Зберегти оригінальні ключі неможливо.

### Дивіться також

-   [AppendIterator::append()](appenditerator.append.md) \- додає ітератор
