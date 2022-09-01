---
navigation:
  - generator.send.md: '« Generator::send'
  - generator.valid.md: 'Generator::valid »'
  - index.md: PHP Manual
  - class.generator.md: Generator
title: 'Generator::throw'
---
# Generator::throw

(PHP 5> = 5.5.0, PHP 7, PHP 8)

Generator::throw — Кинути виняток у генератор

### Опис

```methodsynopsis
public Generator::throw(Throwable $exception): mixed
```

Викидає виняток у генератор та відновлює його виконання. Поведінка буде такою, начебто поточне значення [yield](language.generators.syntax.html#control-structures.yield) замінили на вираз `throw $exception`

Якщо на момент виклику цього методу генератор закритий, виняток буде викинуто в контексті коду, що викликає.

### Список параметрів

`exception`

Виняток, який треба викинути в генератор.

### Значення, що повертаються

Повертає згенероване значення.

### Приклади

**Приклад #1 Викидання виключення в ітератор**

```php
<?php
function gen() {
    echo "Foo\n";
    try {
        yield;
    } catch (Exception $e) {
        echo "Exception: {$e->getMessage()}\n";
    }
    echo "Bar\n";
}

$gen = gen();
$gen->rewind();
$gen->throw(new Exception('Test'));
?>
```

Результат виконання цього прикладу:

```
Foo
Exception: Test
Bar
```
