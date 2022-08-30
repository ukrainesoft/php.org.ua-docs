Отримати унікальний ідентифікатор посилання

-   [« ReflectionReference::fromArrayElement](reflectionreference.fromarrayelement.md)
    
-   [ReflectionAttribute »](class.reflectionattribute.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionReference](class.reflectionreference.md)
    
-   Отримати унікальний ідентифікатор посилання
    

# ReflectionReference::getId

(PHP 7> = 7.4.0, PHP 8)

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

**Приклад #1 Просте використання **ReflectionReference::getId()****

```php
<?php
$val1 = 'foo';
$val2 = 'bar';
$arr = [&$val1, &$val2, &$val1];

$rr1 = ReflectionReference::fromArrayElement($arr, 0);
$rr2 = ReflectionReference::fromArrayElement($arr, 1);
$rr3 = ReflectionReference::fromArrayElement($arr, 2);

var_dump($rr1->getId() === $rr2->getId());
var_dump($rr1->getId() === $rr3->getId());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```