---
navigation:
  - reflectionclass.newinstance.md: '« ReflectionClass::newInstance'
  - reflectionclass.newinstancewithoutconstructor.md: 'ReflectionClass::newInstanceWithoutConstructor »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::newInstanceArgs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::newInstanceArgs

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

ReflectionClass::newInstanceArgs — Створює екземпляр класу з переданими параметрами

### Опис

```methodsynopsis
public ReflectionClass::newInstanceArgs(array $args = []): ?object
```

Створює новий екземпляр класу. Прийняті аргументи передаються конструктор класу.

### Список параметрів

`args`

Масив (array) аргументів, який потім передається конструктор класу.

### Значення, що повертаються

Повертає новий екземпляр класу або \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Якщо конструктор не є public (загальнодоступним), це призведе до генерації винятку [ReflectionException](class.reflectionexception.md)

Якщо конструктор відсутня, а параметр `args` має один і більше аргументів, то це призведе до генерації винятку [ReflectionException](class.reflectionexception.md)

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::newInstanceArgs()\*\*\*\*

```php
<?php
$class = new ReflectionClass('ReflectionFunction');
$instance = $class->newInstanceArgs(array('substr'));
var_dump($instance);
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionFunction)#2 (1) {
  ["name"]=>
  string(6) "substr"
}
```

### Дивіться також

-   [ReflectionClass::newInstance()](reflectionclass.newinstance.md) \- створює екземпляр класу з переданими аргументами
-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.md) \- Створює новий екземпляр класу без виклику конструктора
