Викликає функцію кожного елемента в итераторе

-   [« classuses](function.class-uses.html)
    
-   [iteratorcount »](function.iterator-count.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SPL](ref.spl.md)
    
-   Викликає функцію кожного елемента в итераторе
    

# iteratorapply

(PHP 5> = 5.1.0, PHP 7, PHP 8)

iteratorapply — Викликає функцію кожного елемента в ітераторі

### Опис

```methodsynopsis
iterator_apply(Traversable $iterator, callable $callback, ?array $args = null): int
```

Викликає функцію кожного елемента в итераторе.

### Список параметрів

`iterator`

Об'єкт ітератора для перебору.

`callback`

Функція зворотного дзвінка, яка застосовується до кожного елемента. Ця функція приймає лише переданий `args`тому він null за замовчуванням. Наприклад, якщо `count($args) === 3`, функція зворотного виклику – тернарна.

> **Зауваження**: Функція повинна повертати **`true`** для того, щоб продовжувати процес ітерації над `iterator`

`args`

Аргументи для передачі зворотного дзвінка. Масив (array) аргументів; кожен елемент `args` передається у функцію зворотної функції (`callback`) у вигляді окремого аргументу.

### Значення, що повертаються

Повертає кількість ітерацій.

### Приклади

**Приклад #1 Приклад використання **iteratorapply()****

```php
<?php
function print_caps(Iterator $iterator) {
    echo strtoupper($iterator->current()) . "\n";
    return TRUE;
}

$it = new ArrayIterator(array("Apples", "Bananas", "Cherries"));
iterator_apply($it, "print_caps", array($it));
?>
```

Результат виконання цього прикладу:

```
APPLES
BANANAS
CHERRIES
```

### Дивіться також

-   [arraywalk()](function.array-walk.html) - Застосовує задану користувачем функцію кожного елемента масиву