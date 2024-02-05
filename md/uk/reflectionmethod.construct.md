---
navigation:
  - class.reflectionmethod.md: « ReflectionMethod
  - reflectionmethod.createfrommethodname.md: 'ReflectionMethod::createFromMethodName »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::\_\_construct - Конструктор класу ReflectionMethod

### Опис

public**ReflectionMethod::\_\_construct**(object|string`$objectOrMethod`, string`$method`) .

Alternative signature (not supported with named arguments):

public**ReflectionMethod::\_\_construct**(string`$classMethod`) .

Створює новий об'єкт класу [ReflectionMethod](class.reflectionmethod.md)

### Список параметрів

`objectOrMethod`

Ім'я класу або об'єкт (примірник класу), що містить метод.

`method`

Ім'я методу.

`classMethod`

Імена класу та методу, розділені `::`

### Помилки

Исключение[ReflectionException](class.reflectionexception.md) викидається, якщо заданий метод немає.

### Приклади

**Пример #1 Пример использования**ReflectionMethod::\_\_construct()\*\*\*\*

```php
<?php
class Counter
{
    private static $c = 0;

    /**
     * Счётчик
     *
     * @final
     * @static
     * @access  public
     * @return  int
     */
    final public static function increment()
    {
        return ++self::$c;
    }
}

// Создание экземпляра класса ReflectionMethod
$method = new ReflectionMethod('Counter', 'increment');

// Вывод основной информации
printf(
    "===> %s%s%s%s%s%s%s метод '%s' (%s)\n" .
    "     объявлен в %s\n" .
    "     строки с %d по %d\n" .
    "     имеет модификаторы %d[%s]\n",
        $method->isInternal() ? 'внутренний' : 'определённый пользователем',
        $method->isAbstract() ? ' абстрактный' : '',
        $method->isFinal() ? ' окончательный' : '',
        $method->isPublic() ? ' общедоступный' : '',
        $method->isPrivate() ? ' закрытый' : '',
        $method->isProtected() ? ' защищённый' : '',
        $method->isStatic() ? ' статический' : '',
        $method->getName(),
        $method->isConstructor() ? 'конструктор' : 'обычный метод',
        $method->getFileName(),
        $method->getStartLine(),
        $method->getEndline(),
        $method->getModifiers(),
        implode(' ', Reflection::getModifierNames($method->getModifiers()))
);

// Вывод doc-комментария
printf("---> Комментарий:\n %s\n", var_export($method->getDocComment(), true));

// Вывод статических переменных, если есть
if ($statics= $method->getStaticVariables()) {
    printf("---> Статические переменные: %s\n", var_export($statics, true));
}

// Вызов метода
printf("---> Результат вызова метода: ");
var_dump($method->invoke(NULL));
?>
```

Висновок наведеного прикладу буде схожим на:

```
===> определённый пользователем окончательный общедоступный статический метод 'increment' (обычный метод)
     объявлен в /Users/philip/cvs/phpdoc/test.php
     строки с 14 по 17
     имеет модификаторы 261[final public static]
---> Комментарий:
 '/**
     * Счётчик
     *
     * @final
     * @static
     * @access  public
     * @return  int
     */'
---> Результат вызова метода: int(1)
```

### Дивіться також

-   [ReflectionMethod::export()](reflectionmethod.export.md) \- Експорт відбитого методу
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
