---
navigation:
  - function.class-uses.md: « class\_uses
  - function.iterator-count.md: iterator\_count »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: iterator\_apply
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iterator\_apply

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

iterator\_apply — Викликає функцію кожного елемента в ітераторі

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

**Пример #1 Пример использования**iterator\_apply()\*\*\*\*

```php
<?php
function print_caps(Iterator $iterator) {
    echo strtoupper($iterator->current()) . "\n";
    return TRUE;
}

$it = new ArrayIterator(array("Apples", "Bananas", "Cherries"));
iterator_apply($it, "print_caps", array($it));
?>
```

Результат виконання наведеного прикладу:

```
APPLES
BANANAS
CHERRIES
```

### Дивіться також

-   [array\_walk()](function.array-walk.md) \- Застосовує задану користувачем функцію кожного елемента масиву
