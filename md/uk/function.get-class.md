---
navigation:
  - function.get-class-vars.md: « getclassvars
  - function.get-declared-classes.md: getdeclaredclasses »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getclass
---
# getclass

(PHP 4, PHP 5, PHP 7, PHP 8)

getclass — Повертає ім'я класу, до якого належить об'єкт

### Опис

```methodsynopsis
get_class(object $object = ?): string
```

Повертає ім'я класу, екземпляром якого є об'єкт `object`

### Список параметрів

`object`

Об'єкт, що тестується. Всередині класу цей параметр можна опустити.

> **Зауваження**: Починаючи з PHP 7.2.0, явна передача **`null`** в `object` заборонена та видає помилку рівня **`E_WARNING`**. Починаючи з PHP 8.0.0, під час передачі **`null`**, викидається виняток [TypeError](class.typeerror.md)

### Значення, що повертаються

Повертає ім'я класу, до якого належить екземпляр `object`

Якщо параметр `object` опущений усередині класу, буде повернуто ім'я цього класу.

Якщо параметр `object` є екземпляром класу, що існує у просторі імен, то буде повернуто повне ім'я із зазначенням простору імен.

### Помилки

Якщо функція **getclass()** викликається з чимось, крім об'єкта, викидається виняток [TypeError](class.typeerror.md). До PHP 8.0.0 видавалася помилка рівня **`E_WARNING`**

Якщо функція **getclass()** викликається без аргументів поза класом, викидається виняток [Error](class.error.md). До PHP 8.0.0 видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Виклик функції поза класом без жодних аргументів викликає виняток [Error](class.error.md). Раніше видавалася помилка рівня **`E_WARNING`** та функція повертала значення **`false`** |
|  | До цієї версії значення за замовчуванням для `object` було **`null`** з тим самим ефектом, як і відсутність передачі значення. Тепер **`null`** був видалений як значення за замовчуванням для `object` і більше не є допустимим значенням. |

### Приклади

**Приклад #1 Використання **getclass()****

```php
<?php

class foo {
    function name()
    {
        echo "Меня зовут " , get_class($this) , "\n";
    }
}

// создание объекта
$bar = new foo();

// внешний вызов
echo "Его имя " , get_class($bar) , "\n";

// внутренний вызов
$bar->name();

?>
```

Результат виконання цього прикладу:

```
Его имя foo
Меня зовут foo
```

**Приклад #2 Використання **getclass()** у батьківському класі**

```php
<?php

abstract class bar {
    public function __construct()
    {
        var_dump(get_class($this));
        var_dump(get_class());
    }
}

class foo extends bar {
}

new foo;

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
string(3) "bar"
```

**Приклад #3 Використання **getclass()** з класами у просторах імен**

```php
<?php

namespace Foo\Bar;

class Baz {
    public function __construct()
    {

    }
}

$baz = new \Foo\Bar\Baz;

var_dump(get_class($baz));
?>
```

Результат виконання цього прикладу:

```
string(11) "Foo\Bar\Baz"
```

### Дивіться також

-   [getcalledclass()](function.get-called-class.md) - Ім'я класу, отримане за допомогою пізнього статичного зв'язування
-   [getparentclass()](function.get-parent-class.md) - Повертає ім'я батьківського класу для об'єкта чи класу
-   [gettype()](function.gettype.md) - Повертає тип змінної
-   [getdebugtype()](function.get-debug-type.md) - Повертає ім'я типу змінної у вигляді, що підходить для налагодження
-   [ісsubclassof()](function.is-subclass-of.md) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
