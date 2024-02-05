---
navigation:
  - function.enum-exists.md: « enum\_exists
  - function.get-class-methods.md: get\_class\_methods »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_called\_class
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_called\_class

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

get\_called\_class - Ім'я класу, отримане за допомогою пізнього статичного зв'язування

### Опис

```methodsynopsis
get_called_class(): string
```

Повертає ім'я класу, з якого викликано статичний метод.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я класу.

### Помилки

Якщо функція **get\_called\_class()** викликається не з класу, то видається помилка [Error](class.error.md). До версії PHP 8.0.0 видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Виклик функції не з класу тепер призводить до помилки [Error](class.error.md). . Раніше видавалася помилка рівня **`E_WARNING`** та функція повертала значення **`false`** |

### Приклади

**Пример #1 Пример использования**get\_called\_class()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
string(3) "foo"
string(3) "bar"
```

### Дивіться також

-   [get\_parent\_class()](function.get-parent-class.md) \- Повертає ім'я батьківського класу для об'єкта чи класу
-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [is\_subclass\_of()](function.is-subclass-of.md) \- Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
