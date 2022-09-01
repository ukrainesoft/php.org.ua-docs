---
navigation:
  - arrayaccess.offsetget.md: '« ArrayAccess::offsetGet'
  - arrayaccess.offsetunset.md: 'ArrayAccess::offsetUnset »'
  - index.md: PHP Manual
  - class.arrayaccess.md: ArrayAccess
title: 'ArrayAccess::offsetSet'
---
# ArrayAccess::offsetSet

(PHP 5, PHP 7, PHP 8)

ArrayAccess::offsetSet — Надає значення заданому зміщенню

### Опис

```methodsynopsis
public ArrayAccess::offsetSet(mixed $offset, mixed $value): void
```

Надає значення зазначеному зміщенню (ключу).

### Список параметрів

`offset`

Зміщення (ключ), якому присвоюватиметься значення.

`value`

Значення для присвоєння.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Параметр `offset` буде встановлений у **`null`**, якщо інше значення недоступне, як показано в наведеному нижче прикладі.
> 
> ```php
> <?php
> $arrayaccess[] = "первое значение";
> $arrayaccess[] = "второе значение";
> print_r($arrayaccess);
> ?>
> ```
> 
> Результат виконання цього прикладу:
> 
> ```
> Array
> (
>     [0] => first value
>     [1] => second value
> )
> ```

> **Зауваження**
> 
> Даний метод не викликається при присвоєння за посиланням та інших непрямих змін величин масиву перевантаженого об'єкта [ArrayAccess](class.arrayaccess.md) (Непрямі в тому сенсі, що вони зроблені не прямою заміною величини, а шляхом зміни частина елемента або властивості елемента масиву, або присвоєнням елемента масиву за посиланням іншою зміною). Натомість, викликається метод [ArrayAccess::offsetGet()](arrayaccess.offsetget.md). Ця операція буде успішною лише в тому випадку, якщо метод повертає за посиланням.
