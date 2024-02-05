---
navigation:
  - splfixedarray.serialize.md: '« SplFixedArray::\_\_serialize'
  - splfixedarray.toarray.md: 'SplFixedArray::toArray »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::setSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::setSize

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::setSize — Змінює розмір масиву

### Опис

```methodsynopsis
public SplFixedArray::setSize(int $size): bool
```

Устанавливает размер массива в значение`size`. Якщо `size` менше поточного розміру масиву, всі зайві значення відкидаються. Якщо ж `size` більше поточного розміру масиву, то масив буде доповнено **`null`** значеннями.

### Список параметрів

`size`

Новое значение размера массива. Ожидается значение между и\*\*`PHP_INT_MAX`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), когда`size`меньше нуля.

Викликає помилку рівня **`E_WARNING`**, когда`size` не можна обробити як число.

### Приклади

**Пример #1 Пример использования**SplFixedArray::setSize()\*\*\*\*

```php
<?php
   $array = new SplFixedArray(5);
   echo $array->getSize()."\n";
   $array->setSize(10);
   echo $array->getSize()."\n";
?>
```

Результат виконання наведеного прикладу:

```
5
10
```
