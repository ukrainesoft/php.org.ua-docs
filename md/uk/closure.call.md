---
navigation:
  - closure.bindto.md: '« Closure::bindTo'
  - closure.fromcallable.md: 'Closure::fromCallable »'
  - index.md: PHP Manual
  - class.closure.md: Closure
title: 'Closure::call'
---
# Closure::call

(PHP 7, PHP 8)

Closure::call — Зв'язує та запускає замикання

### Опис

```methodsynopsis
public Closure::call(object $newThis, mixed ...$args): mixed
```

Тимчасово пов'язує замикання з `newThis` та викликає його із заданими параметрами.

### Список параметрів

`newThis`

Об'єкт (object) для прив'язки до замикання під час його виклику.

`args`

Нуль або більше параметрів, що передаються замиканню.

### Значення, що повертаються

Повертає значення замикання, що повертається

### Приклади

**Приклад #1 Приклад **Closure::call()****

```php
<?php
class Value {
    protected $value;

    public function __construct($value) {
        $this->value = $value;
    }

    public function getValue() {
        return $this->value;
    }
}

$three = new Value(3);
$four = new Value(4);

$closure = function ($delta) { var_dump($this->getValue() + $delta); };
$closure->call($three, 4);
$closure->call($four, 4);
?>
```

Результат виконання цього прикладу:

```
int(7)
int(8)
```
