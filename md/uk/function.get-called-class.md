---
navigation:
  - function.enum-exists.md: « enumexists
  - function.get-class-methods.md: getclassmethods »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getcalledclass
---
# getcalledclass

(PHP 5> = 5.3.0, PHP 7, PHP 8)

getcalledclass - Ім'я класу, отримане за допомогою пізнього статичного зв'язування

### Опис

```methodsynopsis
get_called_class(): string
```

Повертає ім'я класу, з якого викликано статичний метод.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я класу. Повертає \*\*`false`\*\*якщо було викликано поза класом.

### Приклади

**Приклад #1 Приклад використання **getcalledclass()****

```php
<?php

class foo {
    static public function test() {
        var_dump(get_called_class());
    }
}

class bar extends foo {
}

foo::test();
bar::test();

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
string(3) "bar"
```

### Дивіться також

-   [getparentclass()](function.get-parent-class.md) - Повертає ім'я батьківського класу для об'єкта чи класу
-   [getclass()](function.get-class.md) - Повертає ім'я класу, до якого належить об'єкт
-   [ісsubclassof()](function.is-subclass-of.md) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
