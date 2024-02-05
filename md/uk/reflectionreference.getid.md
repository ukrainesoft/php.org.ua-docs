---
navigation:
  - reflectionreference.fromarrayelement.md: '« ReflectionReference::fromArrayElement'
  - class.reflectionattribute.md: ReflectionAttribute »
  - index.md: PHP Manual
  - class.reflectionreference.md: ReflectionReference
title: 'ReflectionReference::getId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionReference::getId

(PHP 7 >= 7.4.0, PHP 8)

ReflectionReference::getId — Отримати унікальний ідентифікатор посилання

### Опис

```methodsynopsis
public ReflectionReference::getId(): string
```

Повертає ідентифікатор, що є унікальним для посилання протягом усього життя. Цей ідентифікатор можна використовувати для перевірки на еквівалентність або складання карти відомих посилань.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає string невизначеного формату.

### Приклади

**Пример #1 Простое использование**ReflectionReference::getId()\*\*\*\*

```php
<?php
$val1 = 'foo';
$val2 = 'bar';
$arr = [&$val1, &$val2, &$val1];

$rr1 = ReflectionReference::fromArrayElement($arr, 0);
$rr2 = ReflectionReference::fromArrayElement($arr, 1);
$rr3 = ReflectionReference::fromArrayElement($arr, 2);

var_dump($rr1->getId() === $rr2->getId());
var_dump($rr1->getId() === $rr3->getId());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```
