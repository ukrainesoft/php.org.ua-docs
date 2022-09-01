---
navigation:
  - function.is-a.html: « isа
  - function.method-exists.html: methodexists »
  - index.html: PHP Manual
  - ref.classobj.html: Функції роботи з класами та об'єктами
title: ісsubclassоф
---
# ісsubclassоф

(PHP 4, PHP 5, PHP 7, PHP 8)

ісsubclassof — Перевіряє, чи містить об'єкт у дереві предків зазначений клас чи прямо реалізує його

### Опис

```methodsynopsis
is_subclass_of(mixed $object_or_class, string $class, bool $allow_string = true): bool
```

Перевіряє, чи містить об'єкт `object_or_class` у своєму дереві предків клас `class` або прямо реалізує його.

### Список параметрів

`object_or_class`

Назва класу або екземпляр об'єкта. У разі відсутності такого класу жодної помилки згенеровано не буде.

`class`

Ім'я класу

`allow_string`

Якщо параметр встановлено в false, то не допускається ім'я класу у вигляді рядка як параметр `object_or_class`. Це також запобігає виклику автозавантажувача, якщо клас не існує.

### Значення, що повертаються

Ця функція повертає **`true`**, якщо об'єкт `object_or_class` належить до класу, що успадковує від `class`, інакше вона повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ісsubclassof()****

```php
<?php
// объявляем класс
class WidgetFactory
{
  var $oink = 'moo';
}

// объявляем наследника
class WidgetFactory_Child extends WidgetFactory
{
  var $oink = 'oink';
}

// создаём новый объект
$WF = new WidgetFactory();
$WFC = new WidgetFactory_Child();

if (is_subclass_of($WFC, 'WidgetFactory')) {
  echo "да, \$WFC наследует WidgetFactory\n";
} else {
  echo "нет, \$WFC не наследует WidgetFactory\n";
}


if (is_subclass_of($WF, 'WidgetFactory')) {
  echo "да, \$WF наследует WidgetFactory\n";
} else {
  echo "нет, \$WF не наследует WidgetFactory\n";
}

if (is_subclass_of('WidgetFactory_Child', 'WidgetFactory')) {
  echo "да, WidgetFactory_Child наследует WidgetFactory\n";
} else {
  echo "нет, WidgetFactory_Child не наследует WidgetFactory\n";
}
?>
```

Результат виконання цього прикладу:

```
да, $WFC наследует WidgetFactory
нет, $WF не наследует WidgetFactory
да, WidgetFactory_Child наследует WidgetFactory
```

**Приклад #2 Приклад використання **ісsubclassof()** з інтерфейсами**

```php
<?php
// Определяем интерфейс
interface MyInterface
{
  public function MyFunction();
}

// Определяем класс с реализацией интерфейса
class MyClass implements MyInterface
{
  public function MyFunction()
  {
    return "MyClass реализует MyInterface!";
  }
}

// Создаём объект
$my_object = new MyClass;

// Код ниже работает с PHP 5.3.7

// Проверка с помощью экземпляра объекта
if (is_subclass_of($my_object, 'MyInterface')) {
  echo "Да, \$my_object является подклассом MyInterface\n";
} else {
  echo "Нет, \$my_object не является подклассом MyInterface\n";
}

// Проверка с помощью имени класса в виде строки
if (is_subclass_of('MyClass', 'MyInterface')) {
  echo "Да, MyClass является подклассом MyInterface\n";
} else {
  echo "Нет, MyClass не является подклассом MyInterface\n";
}
?>
```

Результат виконання цього прикладу:

```
Да, $my_object является подклассом MyInterface
Да, MyClass является подклассом MyInterface
```

### Примітки

> **Зауваження**
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функции автозагрузки](language.oop5.autoload.html)якщо клас ще не відомий.

### Дивіться також

-   [getclass()](function.get-class.html) - Повертає ім'я класу, до якого належить об'єкт
-   [getparentclass()](function.get-parent-class.html) - Повертає ім'я батьківського класу для об'єкта чи класу
-   [ісa()](function.is-a.html) - Перевіряє, чи належить об'єкт до цього класу чи чи є цей клас одним із його батьків
-   [classparents()](function.class-parents.html) - Повертає список батьківських класів заданого класу
