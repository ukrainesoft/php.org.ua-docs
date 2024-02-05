---
navigation:
  - function.is-a.md: « is\_a
  - function.method-exists.md: method\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: is\_subclass\_of
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_subclass\_of

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_subclass\_of — Перевіряє, чи містить об'єкт у дереві предків зазначений клас чи прямо реалізує його

### Опис

```methodsynopsis
is_subclass_of(mixed $object_or_class, string $class, bool $allow_string = true): bool
```

Перевіряє, чи містить об'єкт `object_or_class` у своєму дереві предків клас `class`либо прямо реализует его.

### Список параметрів

`object_or_class`

Назва класу або екземпляр об'єкта. У разі відсутності такого класу жодної помилки згенеровано не буде.

`class`

Ім'я класу

`allow_string`

Если параметр установлен в false, то не допускается имя класса в виде строки в качестве параметра`object_or_class`. Це також запобігає виклику автозавантажувача, якщо клас не існує.

### Значення, що повертаються

Ця функція повертає **`true`**, якщо об'єкт `object_or_class`принадлежит к классу, наследующему от`class`, інакше вона повертає **`false`**

### Приклади

**Пример #1 Пример использования**is\_subclass\_of()\*\*\*\*

```php
<?php
// объявляем класс
class WidgetFactory
{
  var $oink = 'moo';
}

// объявляем наследника
class WidgetFactory_Child extends WidgetFactory
{
  var $oink = 'oink';
}

// создаём новый объект
$WF = new WidgetFactory();
$WFC = new WidgetFactory_Child();

if (is_subclass_of($WFC, 'WidgetFactory')) {
  echo "да, \$WFC наследует WidgetFactory\n";
} else {
  echo "нет, \$WFC не наследует WidgetFactory\n";
}


if (is_subclass_of($WF, 'WidgetFactory')) {
  echo "да, \$WF наследует WidgetFactory\n";
} else {
  echo "нет, \$WF не наследует WidgetFactory\n";
}

if (is_subclass_of('WidgetFactory_Child', 'WidgetFactory')) {
  echo "да, WidgetFactory_Child наследует WidgetFactory\n";
} else {
  echo "нет, WidgetFactory_Child не наследует WidgetFactory\n";
}
?>
```

Результат виконання наведеного прикладу:

```
да, $WFC наследует WidgetFactory
нет, $WF не наследует WidgetFactory
да, WidgetFactory_Child наследует WidgetFactory
```

**Пример #2 Пример использования**is\_subclass\_of()\*\* з інтерфейсами\*\*

```php
<?php
// Определяем интерфейс
interface MyInterface
{
  public function MyFunction();
}

// Определяем класс с реализацией интерфейса
class MyClass implements MyInterface
{
  public function MyFunction()
  {
    return "MyClass реализует MyInterface!";
  }
}

// Создаём объект
$my_object = new MyClass;

// Код ниже работает с PHP 5.3.7

// Проверка с помощью экземпляра объекта
if (is_subclass_of($my_object, 'MyInterface')) {
  echo "Да, \$my_object является подклассом MyInterface\n";
} else {
  echo "Нет, \$my_object не является подклассом MyInterface\n";
}

// Проверка с помощью имени класса в виде строки
if (is_subclass_of('MyClass', 'MyInterface')) {
  echo "Да, MyClass является подклассом MyInterface\n";
} else {
  echo "Нет, MyClass не является подклассом MyInterface\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Да, $my_object является подклассом MyInterface
Да, MyClass является подклассом MyInterface
```

### Примітки

> **Зауваження** :
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функції автозавантаження](language.oop5.autoload.md)якщо клас ще не відомий.

### Дивіться також

-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [get\_parent\_class()](function.get-parent-class.md) \- Повертає ім'я батьківського класу для об'єкта чи класу
-   [is\_a()](function.is-a.md) \- Перевіряє, чи об'єкт належить до типу або підтипу
-   [class\_parents()](function.class-parents.md) \- Повертає список батьківських класів заданого класу
