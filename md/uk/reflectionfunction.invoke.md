---
navigation:
  - reflectionfunction.getclosure.md: '« ReflectionFunction::getClosure'
  - reflectionfunction.invokeargs.md: 'ReflectionFunction::invokeArgs »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::invoke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunction::invoke

(PHP 5, PHP 7, PHP 8)

ReflectionFunction::invoke — Викликає функцію

### Опис

```methodsynopsis
public ReflectionFunction::invoke(mixed ...$args): mixed
```

Викликає відбиту (reflected) функцію.

### Список параметрів

`args`

Передані функції аргументи. Може приймати змінну кількість аргументів за аналогією до [call\_user\_func()](function.call-user-func.md)

### Значення, що повертаються

Повертає результат виконання викликаної функції.

### Приклади

**Пример #1 Пример использования**ReflectionFunction::invoke()\*\*\*\*

```php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

$function = new ReflectionFunction('title');

echo $function->invoke('Dr', 'Phil');
?>
```

Результат виконання наведеного прикладу:

```
Dr. Phil
```

### Примітки

> **Зауваження** :
> 
> **ReflectionFunction::invoke()** не можна використовувати, якщо очікуються параметри посилання. Замість нього слід використовувати [ReflectionFunction::invokeArgs()](reflectionfunction.invokeargs.md) (Передача посилань у списку аргументів).

### Дивіться також

-   [ReflectionFunction::export()](reflectionfunction.export.md) \- Експортує функції
-   [\_\_invoke()](language.oop5.magic.md#object.invoke)
-   [call\_user\_func()](function.call-user-func.md) \- Викликає callback-функцію, задану у першому параметрі
